---
description: 元件資料表會列出元件，並具有下列資料行。
ms.assetid: 069d64e9-106a-42b7-8dea-a44fc0c6e0cd
title: 元件資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04e7abe895981f04adc345f7fd54924c93e9c06e2d5e0051c33345c9d3baadce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144736"
---
# <a name="component-table"></a>元件資料表

元件資料表會列出元件，並具有下列資料行。



| Column      | 類型                         | 答案 | Nullable |
|-------------|------------------------------|-----|----------|
| 元件   | [識別碼](identifier.md) | Y   | N        |
| ComponentId | [GUID](guid.md)             | N   | Y        |
| 目錄\_ | [識別碼](identifier.md) | N   | N        |
| 屬性  | [整數](integer.md)       | N   | N        |
| 條件   | [Condition](condition.md)   | N   | Y        |
| KeyPath     | [識別碼](identifier.md) | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>元件
</dt> <dd>

識別元件記錄。

主表索引鍵。

</dd> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId
</dt> <dd>

此元件、版本和語言特有的字串 GUID。

請注意，這些 Guid 的字母必須為大寫。 GUIDGEN 之類的公用程式可以產生包含小寫字母的 Guid。 小寫字母必須變更為大寫才能讓這些有效的元件程式碼 Guid。

如果這個資料行是 null，安裝程式就不會註冊元件，而且安裝程式無法移除或修復元件。 如果只有在安裝期間才需要元件，例如可清除暫存檔或移除舊產品的自訂動作，則可能會刻意完成這項操作。 將資料檔案複製到不需要註冊的使用者電腦時，也可能很有用。

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>目錄\_
</dt> <dd>

[目錄資料表](directory-table.md)中專案的外部索引鍵。 這是屬性名稱，其值包含實際的路徑，可以透過 [AppSearch 動作](appsearch-action.md) 或從目錄資料表取得的預設設定來設定。

開發人員必須避免撰寫將檔案放入其中一個使用者設定檔資料夾的元件。 在多使用者的情況下，所有使用者都無法使用這些檔案，而且可能會導致安裝程式將元件永久視為需要修復。

目錄資料表中第一個資料行的外部索引鍵。

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性
</dt> <dd>

此資料行包含一個位旗標，可指定遠端執行的選項。 將指定的位新增至資料行中的總計值，以包含選項。

> [!Note]  
> 如果是從 web 位置下載 .msi 檔案，則不應將屬性旗標設定為允許從來源執行元件。 這是 Windows Installer 的限制，而且可能會傳回 INSTALLSTATE BADCONFIG 的功能狀態 \_ 。

 



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>位旗標</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesLocalOnly</strong></dt> <dt>0</dt> <dt>0x0000</dt> </dl> 元件無法從來源執行。 針對屬於某項功能的所有元件設定此位，以防止此功能從網路或從來源執行。 請注意，如果功能沒有元件，則此功能一律會顯示從來源執行，並從我的電腦執行為有效的選項。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributesSourceOnly</strong></dt> <dt>1</dt> <dt>0x0001</dt> </dl> 元件只能從來源執行。 針對屬於某項功能的所有元件設定此位，以防止從我的電腦執行此功能。 請注意，如果功能沒有元件，則此功能一律會顯示從來源執行，並從我的電腦執行為有效的選項。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesOptional</strong></dt> <dt>2</dt> <dt>0x0002</dt> </dl> 元件可以在本機或從來源執行。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributesRegistryKeyPath</strong></dt> <dt>4</dt> <dt>0x0004</dt> </dl> 如果設定此位，則 KeyPath 資料行中的值會當做登錄 <a href="registry-table.md">表</a>中的索引鍵使用。 如果登錄資料表中對應記錄的值欄位為 null，則該記錄中的名稱欄位不能包含 &quot; + &quot; 、 &quot; - &quot; 或 &quot; * &quot; 。 如需詳細資訊，請參閱登錄 <a href="registry-table.md">表</a>中的名稱欄位描述。<br/> 建議將此位設定為寫入 HKCU hive 的登錄專案。 這可確保當相同電腦上有多個使用者時，安裝程式會寫入必要的 HKCU 登錄專案。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesSharedDllRefCount</strong></dt> <dt>8</dt> <dt>0x0008</dt> </dl> 如果設定此位，安裝程式會在元件金鑰檔的共用 DLL 登錄中遞增參考計數。 如果未設定此位，則只有在參考計數已經存在時，安裝程式才會遞增參考計數。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributesPermanent</strong></dt> <dt>16</dt> <dt>0x0010</dt> </dl> 如果設定此位，安裝程式就不會在卸載期間移除元件。 安裝程式會在 Windows Installer 登錄設定中為元件註冊額外的系統用戶端。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesODBCDataSource</strong></dt> <dt>32</dt> <dt>0x0020</dt> </dl> 如果設定此位，KeyPath 資料行中的值就是 <a href="odbcdatasource-table.md">ODBCDataSource 資料表</a>中的索引鍵。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributesTransitive</strong></dt> <dt>64</dt> <dt>0x0040</dt> </dl> 如果設定此位，則安裝程式會在重新安裝時重新評估 [條件] 資料行中的語句值。 如果值先前是 False，且已變更為 True，則安裝程式會安裝元件。 如果值先前是 True 且已變更為 False，即使元件有其他產品做為用戶端，安裝程式也會移除該元件。<br/> 此位應該只針對可轉移的元件進行設定。 請參閱 <a href="using-transitive-components.md">使用可轉移的元件</a>。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesNeverOverwrite</strong></dt> <dt>128</dt> <dt>0x0080</dt> </dl> 如果設定此位，則如果元件的金鑰路徑檔案或機碼路徑登錄專案已經存在，安裝程式就不會安裝或重新安裝元件。 應用程式會將本身註冊為元件的用戶端。<br/> 只有登錄資料表所註冊的元件才能使用此旗標。 請勿將此旗標用於 <a href="appid-table.md">AppId</a>、 <a href="class-table.md">類別</a>、 <a href="extension-table.md">延伸</a>模組、 <a href="progid-table.md">ProgId</a>、 <a href="mime-table.md">MIME</a>和 <a href="verb-table.md">動詞資料表</a>所註冊的元件。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributes64bit</strong></dt> <dt>256</dt> <dt>0x0100</dt> </dl> 設定此位以將此標示為64位元件。 這個屬性可協助安裝包含32位和64位元件的封裝。 如果未設定此位，則會將元件註冊為32位元件。<br/> 如果這是取代32位元件的64位元件，請在 [元件] 資料行中設定此位並指派新的 GUID。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesDisableRegistryReflection</strong></dt> <dt>512</dt> <dt>0x0200</dt> </dl> 設定此位可針對受此元件影響的所有現有和新登錄機碼停用登錄 <a href="/windows/desktop/WinProg64/registry-reflection">反映</a> 。 如果設定此位，Windows Installer 會在元件所存取的每個索引鍵上呼叫<a href="/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey"><strong>RegDisableReflectionKey</strong></a> 。 這位 Windows Installer 版本4.0 提供。 32位系統會忽略此位。 在 Windows XP 的64位版本上，會忽略這個位。<br/>
<blockquote>
[!Note]<br />
32位 Windows 在64位 Windows 模擬器上執行的應用程式 (WOW64) 參考不同于64位應用程式的登錄。 登錄反映會複製這兩個登錄視圖之間的一些登錄值。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>msidbComponentAttributesUninstallOnSupersedence</strong></dt> <dt>1024</dt> <dt>0x0400</dt> </dl> 為修補程式套件中的元件設定此位，以避免在電腦上留下孤立的元件。 如果已安裝後續修補程式，並在其<a href="msipatchsequence-table.md">MsiPatchSequence</a>資料表中標示<strong>msidbPatchSequenceSupersedeEarlier</strong>值來取代第一個修補程式，Windows Installer 4.5 和更新版本可以取消註冊並卸載以<strong>msidbComponentAttributesUninstallOnSupersedence</strong>值標示的元件。 如果元件未標示此位，則取代修補程式的安裝可能會離開電腦上未使用的元件。<br/> 設定 <strong>MSIUNINSTALLSUPERSEDEDCOMPONENTS</strong> 屬性的效果與設定所有元件的這個位相同。<br/> <strong><a href="not-supported-in-windows-installer-4-0.md">Windows Installer 4.0 及更早版本</a>：</strong>不支援<strong>msidbComponentAttributesUninstallOnSupersedence</strong>值，且會忽略。<br/> <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>msidbComponentAttributesShared</strong></dt> <dt>2048</dt> <dt>0x0800</dt> </dl> 如果元件在至少一個安裝于系統上的封裝中以此屬性值標示，則安裝程式會將元件視為所有封裝中標示的元件。 如果已卸載共用標示元件的套件，Windows Installer 4.5 可繼續在系統上共用元件的最高版本，即使是由正在卸載的封裝所安裝的最高版本。 <br/> 如果 DisableSharedComponent 原則設定為1，則沒有任何套件會取得此位啟用的共用元件功能。<br/> <strong><a href="not-supported-in-windows-installer-4-0.md">Windows Installer 4.0 及更早版本</a>：</strong>不支援<strong>msidbComponentAttributesShared</strong>值，且會忽略。<br/> <br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件
</dt> <dd>

此資料行包含可控制是否已安裝元件的條件陳述式。 如果條件為 null 或評估為 true，則會啟用元件。 如果條件評估為 False，則元件已停用且未安裝。

[條件] 欄位只會在 [CostFinalize 動作](costfinalize-action.md)期間啟用或停用元件。 若要在 CostFinalize 之後啟用或停用元件，您必須使用自訂動作或 [Dataadapter.doaction ControlEvent](doaction-controlevent.md) 來呼叫 [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)。

請注意，除非為元件設定 [屬性] 資料行中的可轉移位，否則即使在 [條件] 資料行中的條件陳述式之後，會在產品的後續維護安裝中評估為 False，仍然會在安裝後啟用此元件。

元件資料表中的 [條件] 資料行接受條件運算式，其中包含已安裝的功能和元件狀態的參考。 如需條件陳述式語法的詳細資訊，請參閱 [條件陳述式語法](conditional-statement-syntax.md)。

</dd> <dt>

<span id="KeyPath"></span><span id="keypath"></span><span id="KEYPATH"></span>KeyPath
</dt> <dd>

這個值指向安裝程式用來偵測元件的檔案或資料夾。 兩個元件不能共用相同的索引鍵路徑值。 此資料行中的值也是 [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) 函數所傳回的路徑。

如果值不是 null，則根據屬性值，KeyPath 就會是登錄、 [ODBCDataSource](odbcdatasource-table.md)或檔案[資料表](file-table.md)[中的主鍵](registry-table.md)。 如果 KeyPath 為 null，則會使用目錄資料行的資料夾 \_ 做為金鑰路徑。

因為安裝程式所建立的資料夾是空的，所以您必須在 [CreateFolder 資料表](createfolder-table.md) 中撰寫一個專案，才能安裝包含空資料夾的元件。

請注意，如果 Windows Installer 元件包含受[Windows 資源保護](/windows/desktop/Wfp/windows-resource-protection-portal) (WRP) 的檔案或登錄機碼，或受 Windows 檔案保護 (WFP) 保護的檔案，則必須使用此資源做為元件的 KeyPath。 在此情況下，Windows Installer 不會安裝、更新或移除元件。 您不應該在安裝套件中包含任何受保護的資源。 相反地，您應該針對 Windows 資源保護使用[支援的資源取代機制](/windows/desktop/Wfp/supported-file-replacement-mechanisms)。 如需詳細資訊，請參閱[使用 Windows Installer 和 Windows 資源保護](windows-resource-protection-on-windows-vista.md)。

</dd> </dl>

## <a name="remarks"></a>備註

如需元件和功能之間關聯性的討論，請參閱 [功能表](feature-table.md)。

安裝程式會持續追蹤共用 Dll，而不受登錄中的共用 DLL 參考計數影響。 如果有共用 DLL 的參考計數存在於登錄中，安裝程式會在安裝檔案時，一律遞增計數，並在卸載時將其遞減。 如果未設定 **msidbComponentAttributesSharedDllRefCount**，而且參考計數尚未存在，安裝程式將不會建立該參考計數。 請注意，所有安裝到系統資料夾的檔案，登錄中的 Shareddll 參考計數都會遞增。

如果未設定 **msidbComponentAttributesSharedDllRefCount** ，則其他應用程式即使仍然需要，也可以移除該元件。 若要瞭解如何發生這種情況，請考慮下列案例：

-   使用安裝程式的應用程式會安裝共用元件。
-   未設定 **msidbComponentAttributesSharedDllRefCount** 位，而且沒有參考計數。 因此，安裝程式不會開始參考計數。
-   會安裝共用此元件且不使用安裝程式的繼承應用程式。
-   繼承應用程式會建立並遞增共用元件的參考計數。
-   卸載繼承應用程式。
-   共用元件的參考計數會減少為零，而且會移除該元件。
-   使用安裝程式的應用程式不再具有元件的存取權。

若要避免此行為，請設定 **msidbComponentAttributesSharedDllRefCount**。

請注意，系統服務元件不應指定為從來源執行，而不需要特別針對這類用途所設計。 如需詳細資訊，請參閱 [ServiceInstall 資料表](serviceinstall-table.md) 。

請注意，對於包含進入系統資料夾的動態連結程式庫的元件，一律不應設定啟用從來源執行安裝的屬性。 原因是，如果元件的安裝狀態變成設定為從來源執行（藉由遵循某項功能或在 UI 中設定），則在 DLL 上對 **LoadLibrary** 的後續呼叫會失敗。

另請參閱 [控制特徵選取狀態](controlling-feature-selection-states.md)。

## <a name="validation"></a>驗證

<dl>

[ICE02](ice02.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE08](ice08.md)  
[ICE09](ice09.md)  
[ICE18](ice18.md)  
[ICE19](ice19.md)  
[ICE21](ice21.md)  
[ICE30](ice30.md)  
[ICE32](ice32.md)  
[ICE35](ice35.md)  
[ICE38](ice38.md)  
[ICE41](ice41.md)  
[ICE42](ice42.md)  
[ICE43](ice43.md)  
[ICE46](ice46.md)  
[ICE50](ice50.md)  
[ICE54](ice54.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE62](ice62.md)  
[ICE67](ice67.md)  
[ICE76](ice76.md)  
[ICE79](ice79.md)  
[ICE80](ice80.md)  
[ICE83](ice83.md)  
[ICE86](ice86.md)  
[ICE88](ice88.md)  
[ICE91](ice91.md)  
[ICE92](ice92.md)  
[ICE97](ice97.md)  
</dl>

