# パフォーマンスモニタによる監視

本節では、パフォーマンスモニタにて連続稼働中のプログラムの挙動の変化を監視し、システムに悪い影響を及ば差ないか監視するための設定手順を示します。
連続稼働によりログは非常に大きなサイズを占めますので、この手順では ``D:`` ドライブとして外付けストレージを設置し、そこへ記録するものとして説明します。


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>スタートメニューより検索を選び、 <code>perfmon</code> と入力</td>
<td></td>
</tr>
<tr class="even">
<td><code>User Defined</code> から
<code>New &gt; Data Collector Set</code> を選択して <code>Next</code>
ボタンを押す</td>
<td><img src="image/1_add_user_defined_monitor.png" class="align-center"
alt="image" /></td>
</tr>
<tr class="odd">
<td><code>Name:</code> に適当な名前（初期値のままで良い）を設定し、
<code>Create from a template</code> が選択された状態で <code>Next</code>
ボタンを押す</td>
<td><img src="image/2_collection_type_name_setting.png"
class="align-center" alt="image" /></td>
</tr>
<tr class="even">
<td><code>System Diagnostics</code> を選択して <code>Next</code>
ボタンを押す</td>
<td><img src="image/3_select_template.png" class="align-center"
alt="image" /></td>
</tr>
<tr class="odd">
<td><code>Root directory:</code> 入力項目で、 <code>%systemdrive%</code>
の部分を外付ストレージのドライブレターへ変更して <code>Next</code>
ボタンを押す</td>
<td><img src="image/4_define_save_drive.png" class="align-center"
alt="image" /></td>
</tr>
<tr class="even">
<td><code>Save and close</code> を選択して <code>Finish</code>
ボタンを押す</td>
<td><img src="image/5_save.png" class="align-center" alt="image" /></td>
</tr>
<tr class="odd">
<td><code>User Defined</code> フォルダ下に作成した
<code>New Data Collector Set</code>
が追加されるため、右クリックして現れたポップアップメニューから
<code>Properties</code> を選択</td>
<td><img src="image/6_property.png" class="align-center"
alt="image" /></td>
</tr>
<tr class="even">
<td><code>Stop Condition</code><span class="title-ref">
タブを開き、次の通り設定変更したあと、 </span><span
class="title-ref">Apply</span><span class="title-ref"> , </span><span
class="title-ref">OK</span>` ボタンを順にを押す
<dl>
<dt>Overall duration</dt>
<dd>
<p>ON &gt; OFF</p>
</dd>
<dt>Restart the data collector set at limits.</dt>
<dd>
<p>OFF &gt; ON</p>
</dd>
<dt>Duration</dt>
<dd>
<p>ON &gt; OFF</p>
</dd>
<dt>Maximum Size</dt>
<dd>
<p>OFF &gt; ON, 小分けにしたいログサイズ</p>
</dd>
<dt>Stop when all data collections have finished.</dt>
<dd>
<p>ON &gt; OFF</p>
</dd>
</dl></td>
<td><img src="image/7_stop_condition.png" class="align-center"
alt="image" /></td>
</tr>
<tr class="odd">
<td>再度 <code>New Data Collector Set</code> を右クリックし、
<code>Start</code>
を選択する。これにより指定したフォルダパスへログが出力される。以後小分けにしたサイズ毎にフォルダが分かれてログを保存する。</td>
<td><img src="image/8_start_logging.png" class="align-center"
alt="image" /></td>
</tr>
</tbody>
</table>

!!! Warning
    外付ドライブを取り外す際は、事前に `perfmon` を起動し、 `User Defined > New Data Collector Set` を右クリックし、 `Stop` を行い、ログ記録を停止させてください。
