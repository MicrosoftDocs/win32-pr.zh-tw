---
description: Mt.exe 檔案是產生已簽署檔案和目錄的工具。 它可在 Microsoft Windows 軟體開發套件 (SDK) 中取得。 Mt.exe 要求資訊清單中所參考的檔案必須存在於與資訊清單相同的目錄中。
ms.assetid: 37f010ee-2658-4547-9871-c913201042de
title: Mt.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df654a943bad272a091dc6ac20cc1dcdab1731a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986288"
---
# <a name="mtexe"></a>Mt.exe

Mt.exe 檔案是產生已簽署檔案和目錄的工具。 它可在 Microsoft Windows 軟體開發套件 (SDK) 中取得。 Mt.exe 要求資訊清單中所參考的檔案必須存在於與資訊清單相同的目錄中。

Mt.exe 使用 (SHA-1) 的安全雜湊演算法 CryptoAPI 執行來產生雜湊。 如需雜湊演算法的詳細資訊，請參閱 [雜湊和](/windows/desktop/SecCrypto/hash-and-signature-algorithms)簽章演算法。 雜湊會以十六進位字串的形式插入資訊清單中的 **檔案標記。** 此工具目前只會產生 SHA-1 雜湊，雖然資訊清單中的檔案可能會使用其他雜湊配置。

Mt.exe 使用 Makecat.exe 來產生類別目錄檔案， ( 的類別目錄定義檔案中) 的 (。 此工具會以您的資訊清單名稱和位置填滿標準範本 CDF。 您可以使用此 Makecat.exe 來產生元件類別目錄。

最新版本的 Windows SDK 提供的 Mt.exe 版本也可以用來產生 managed 元件和非受控並存元件的資訊清單。

## <a name="syntax"></a>Syntax

**mt.exe \[ 資訊清單**_<component1 資訊清單><component2>_ *_\] \[ -identity：_* *<identity string> * **\] \[ -rgs：** _<file1。 rgs>_* _\] \[ -tlb：_ *_<file2 .tlb>_* _\] \[ -dll：_ *_<file3.dll>_* _\] \[ -取代：_ *_<XML filename>_* _\] \[ -managedassemblyname：_ *_<managed assembly>_* _\] \[ -nodependency \] \[ -category \] \[ -out：_ - *_<output manifest name>_* _\] \[ inputresource：_ *_<file4>_* _; \[ \# \]_*_><0 資源 \_ 識別碼><1_* _\] \[ -outputresource：_ *_<file5>_* _\[ \# ; \]_*_><2 資源 \_ 識別碼><3_* _\] \[ -updateresource：_ *_<file6>_* _\[ \# ; \]_*_><4 資源 \_ 識別碼><5_* _\] \[ -hashupdate \[ ：_ *_<path to files>_* _\] \] \[ -makecdfs \] \[ -驗證 \_ 資訊清單 \] \[ -驗證檔案 \_ \_ 雜湊：_ *_<path to files>_* _\] \[ -正常化 \] \[ -檢查 \_ \_ 重複項 \] \[ -nologo \] \[ -verbose \]_*

## <a name="command-line-options"></a>命令列選項

Mt.exe 會使用下列不區分大小寫的命令列選項。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>選項</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-manifest</td>
<td>指定資訊清單檔的名稱。 若要修改單一資訊清單，請指定一個資訊清單檔案名。 例如，元件資訊清單。<br/> 若要合併多個資訊清單，請在此指定來源資訊清單的名稱。 使用 <strong>-out</strong>、 <strong>-outputresource</strong>或 <strong>-updateresource</strong> 選項，指定已更新資訊清單的名稱。 例如，下列命令列要求的作業會將兩個資訊清單（man1）和 man2 合併到新的資訊清單 man3 中。<br/> <strong>mt.exe 資訊清單 man1. 資訊清單 man2： man3。資訊清單</strong><br/>
<blockquote>
[!Note]<br />
無冒號 (：使用 <strong>-manifest</strong> 選項時需要 ) 。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>-identity</td>
<td>提供資訊清單之 <strong>assemblyIdentity</strong> 元素的屬性值。 <strong>-Identity</strong>選項的引數是字串值，其中包含以逗號分隔之欄位中的屬性值。 在第一個欄位中提供 <strong>name</strong> 屬性的值，而不包含 &quot; name = &quot; substring。 其餘所有的欄位都會使用下列格式來指定屬性和其值： <em> <attribute name> </em> = <em> <attribute_value> </em> 。<br/> 例如，若要以下列資訊更新資訊清單的 <strong>assemblyIdentity</strong> 元素：<br/> <assemblyIdentity type=&quot;win32&quot; name=&quot;Microsoft.Windows.SampleAssembly&quot; version=&quot;6.0.0.0&quot; processorArchitecture=&quot;x86&quot; publicKeyToken=&quot;a5aaf5ba15723d5&quot;/> <br/> 在命令列上包含下列 <strong>-identity</strong> 選項：<br/> <strong>-identity：</strong> &quot;SampleAssembly、processorArchitecture = x86、version = 6.0.0.0、type = win32、publicKeyToken = a5aaf5ba15723d5&quot;<br/></td>
</tr>
<tr class="odd">
<td>-rgs</td>
<td>指定登入指令檔 ( .rgs) 檔案的名稱。 需要 <strong>-dll</strong> 選項才能使用 <strong>-rgs</strong> 選項。<br/></td>
</tr>
<tr class="even">
<td>-tlb</td>
<td>指定類型程式庫檔案 (.tlb) 的名稱。 需要 <strong>-dll</strong> 選項才能使用 <strong>-tlb</strong> 選項。<br/></td>
</tr>
<tr class="odd">
<td>-dll</td>
<td>指定動態連結程式庫 (DLL) 檔的名稱。 如果使用<strong>-rgs</strong>或<strong>-tlb</strong>選項， <strong>mt.exe</strong>需要<strong>-dll</strong>選項。 指定您想要從 .rgs 或 .tlb 檔案最後建立的 DLL 名稱。<br/> 例如，下列命令會要求從 .rgs 和 .tlb 檔案產生資訊清單的作業。<br/> <strong>mt.exe-rgs： testreg1 .rgs-tlb： testlib1 .tlb -dll:test.dll-取代： rep： &quot; SampleAssembly、processorArchitecture = x86、version = 6.0.0.0、type = win32、publicKeyToken = a5aaf5ba15723d5 &quot; -out： rgstlb. 資訊清單</strong><br/></td>
</tr>
<tr class="even">
<td>-取代</td>
<td>指定檔案，其中包含 .rgs 檔案中可取代字串的值。<br/></td>
</tr>
<tr class="odd">
<td>-managedassemblyname</td>
<td>從指定的受控組件中產生資訊清單。 搭配 <strong>-nodependency</strong> 選項使用，以產生不含相依性元素的資訊清單。 使用 with <strong>-category</strong> 選項來產生具有類別標記的資訊清單。 例如，如果 managed.dll 是 managed 元件，則下列命令列將從 managed.dll 產生 out. 資訊清單。<br/> <strong>mt.exe -managedassemblyname:managed.dll 時： out。資訊清單</strong> <br/></td>
</tr>
<tr class="even">
<td>-nodependency</td>
<td>指定在沒有相依性專案的情況下產生資訊清單的作業。 <strong>-Nodependency</strong>選項需要<strong>-managedassemblyname</strong>選項。 例如，如果 managed.dll 是 managed 元件，則下列命令列將從 managed.dll 產生不具相依性資訊的資訊清單。<br/> <strong>mt.exe -managedassemblyname:managed.dll 時： nodependency</strong><br/></td>
</tr>
<tr class="odd">
<td>-category</td>
<td>指定會產生具有類別標記之資訊清單的作業。 <strong>-Category</strong>選項需要<strong>-managedassemblyname</strong>選項。 例如，如果 managed.dll 是 managed 元件，則下列命令列會從具有類別標記的 managed.dll 產生 out. 資訊清單。<br/> <strong>mt.exe -managedassemblyname:managed.dll 時：. 資訊清單-類別</strong><br/></td>
</tr>
<tr class="even">
<td>-nologo</td>
<td>指定在不顯示標準 Microsoft 著作權資料的情況下執行的操作。 如果 <strong>mt.exe</strong> 在建立程式期間執行，此選項可用來防止將不必要的資訊寫入記錄檔。 <br/></td>
</tr>
<tr class="odd">
<td>-out</td>
<td>指定更新的資訊清單名稱。 如果這是單一資訊清單作業，而且省略了 <strong>-out</strong> 選項，則會修改原始的資訊清單。 <br/></td>
</tr>
<tr class="even">
<td>-inputresource</td>
<td>指定從 RT_MANIFEST 類型的資源取得的資訊清單上執行的作業。 如果使用<strong>-inputresource</strong>選項但未指定資源識別碼，則作業會 <em> <resource_id> </em> 使用 CREATEPROCESS_MANIFEST_RESOURCE 的值。 <br/> 例如，下列命令會要求從 DLL、dll_with_manifest.dll 和資訊清單檔 man2 合併資訊清單的作業。 合併的資訊清單是由另一個 DLL 的資源檔中的資訊清單（dll_with_merged_manifests）所接收。 <br/> <strong>mt.exe -inputresource:dll_with_manifest.dll; #1 資訊清單 man2。資訊清單 -outputresource:dll_with_merged_manifest.dll; #3</strong><br/> 若要從 DLL 解壓縮資訊清單，請指定 DLL 檔案名。 例如，下列命令會從 lib1.dll 解壓縮資訊清單，而 man3 會接收解壓縮的資訊清單。<br/> <strong>mt.exe -inputresource:lib.dll; #1 時： man3 資訊清單</strong><br/></td>
</tr>
<tr class="odd">
<td>-outputresource</td>
<td>指定作業，此作業會產生 RT_MANIFEST 類型的資源所要接收的資訊清單。 如果使用<strong>-outputresource</strong>選項但未指定資源識別碼，則作業會 <em> <resource_id> </em> 使用 CREATEPROCESS_MANIFEST_RESOURCE 的值。 <br/></td>
</tr>
<tr class="even">
<td>-updateresource</td>
<td>指定相當於使用具有相同引數之 <strong>-inputresource</strong> 和 <strong>-outputresource</strong> 選項的作業。 例如，下列命令要求的作業會在指定的路徑上計算檔案的雜湊，並更新可攜式可執行檔 (PE) 的資源資訊清單。<br/> <strong>mt.exe -updateresource:dll_with_manifest.dll; #1-hashupdate： f： \files</strong>。<br/></td>
</tr>
<tr class="odd">
<td>-hashupdate</td>
<td>在指定的路徑上計算檔案的雜湊值，並使用此值更新<strong>File</strong>元素的<strong>hash</strong>屬性值。 <br/> 例如，下列命令會要求合併兩個資訊清單檔案（man1）的作業，並在接收合併資訊的資訊清單中，更新<strong>File</strong>元素的<strong>hash</strong>屬性值。<br/> <strong>mt.exe 資訊清單 man1. 資訊清單 man2. hashupdate： d： \filerepository-out：已合併。資訊清單</strong><br/> 如果未指定檔案的路徑，則作業會搜尋指定之資訊清單的位置以接收更新。 例如，下列命令會要求作業，該作業會使用藉由搜尋已更新之的位置找到的檔案來計算更新的雜湊值。<br/> <strong>mt.exe 資訊清單 yourComponent。資訊清單-hashupdate 時：已更新。資訊清單</strong><br/></td>
</tr>
<tr class="even">
<td>-validate_manifest</td>
<td>指定執行語法檢查是否符合資訊清單架構之資訊清單的作業。 例如，下列命令會要求檢查以驗證 man1 是否符合其架構。 <br/> <strong>mt.exe man1 資訊清單-validate_manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-validate_file_hashes</td>
<td>指定驗證資訊清單之 <strong>File</strong> 元素雜湊值的作業。 例如，下列命令會要求可驗證 man1 之所有 <strong>檔案元素哈</strong> 希值的作業。<br/> <strong>mt.exe 資訊清單 man1。資訊清單-validate_file_hashes： &quot; c; \files&quot;</strong><br/></td>
</tr>
<tr class="even">
<td>-正常化</td>
<td>指定將資訊清單更新為標準格式的操作。 例如，下列命令會將 man1 更新為標準格式。<br/> <strong>mt.exe 資訊清單 man1</strong><br/></td>
</tr>
<tr class="odd">
<td>-check_for_duplicates</td>
<td>指定檢查資訊清單是否有重複元素的作業。 例如，下列命令會檢查 man1 是否有重複的元素。<br/> <strong>mt.exe-man1。資訊清單-check_for_duplicates</strong><br/></td>
</tr>
<tr class="even">
<td>-makecdfs</td>
<td>產生用來建立目錄的 cdf 檔。 例如，在下列命令中，會要求會更新雜湊值並產生 cdf 檔案的作業。<br/> <strong>mt.exe-資訊清單 comp1。資訊清單-hashupdate-makecdfs-out：已更新。資訊清單</strong><br/></td>
</tr>
<tr class="odd">
<td>-verbose</td>
<td>顯示詳細資訊調試資訊。</td>
</tr>
<tr class="even">
<td>-?</td>
<td>使用-?, 或沒有選項和引數來執行時，Mt.exe 會顯示解說文字。</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[並存元件開發工具](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

