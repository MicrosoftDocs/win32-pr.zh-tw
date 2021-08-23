---
description: SNMP 編譯器會以命令列模式以單一可執行檔的形式執行。
ms.assetid: 0e85fe84-dacb-4720-8242-ffa0046780f3
ms.tgt_platform: multiple
title: smi2smir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3909ef1df4047ba0b797fe4a01088c62e60b287969445d311214180e4fa441a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050166"
---
# <a name="smi2smir"></a>smi2smir

SNMP 編譯器會以命令列模式以單一可執行檔的形式執行。 編譯器會接受一個 SNMP 資訊模組作為輸入，並接受解析外部參考所需的任何其他模組。 使用下列其中一個命令列語法範例。

如需有關如何使用這個編譯器的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。

``` syntax
smi2smir [<DiagnosticArgs>] [<VersionArgs>]
     <CommandArgs> <MIB file> [<Import Files>]

smi2smir [<DiagnosticArgs>] <RegistryArgs> [<Directory>]

smi2smir <ModuleInfoArgs> <MIB file>

smi2smir <HelpArgs>
```

## <a name="switches"></a>交換器

<dl> <dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*DiagnosticArgs*>
</dt> <dd>

編譯器接受下列診斷引數。

<dl> <dt>

<span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<**_診斷層級_*_>_*
</dt> <dd>

要顯示的診斷類型。 預設值為 2。

以下是可以設定的診斷層級值清單：

-   0 = 無訊息
-   1 = 嚴重
-   2 = 嚴重和警告
-   3 = 嚴重、警告和資訊訊息

</dd> <dt>

<span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<**_計數_*_>_*
</dt> <dd>

要顯示的最大嚴重訊息和警告訊息數目; *計數* 必須是正整數整數。 如果未指定 **/c** ，可以回報的錯誤數目沒有任何限制。

</dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*VersionArgs*>
</dt> <dd>

編譯器接受下列版本引數。

<dl> <dt>

<span id="_v1"></span><span id="_V1"></span>**/v1**
</dt> <dd>

指定嚴格符合 SNMPv1 SMI-S。 如果編譯器偵測到非 SNMPv1 語句，則會報告錯誤。

</dd> <dt>

<span id="_v2c"></span><span id="_V2C"></span>**/v2c**
</dt> <dd>

指定對 SNMPv2 SMI-S 的嚴格一致性。 如果編譯器偵測到非 SNMPv2 語句，則會報告錯誤。

</dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*CommandArgs*>
</dt> <dd>

編譯器接受下列命令引數。

<dl> <dt>

<span id="_d"></span><span id="_D"></span>**/d**
</dt> <dd>

從 SMIR 中刪除指定的模組。

</dd> <dt>

<span id="_p"></span><span id="_P"></span>**/p**
</dt> <dd>

刪除 SMIR 中的所有模組。

</dd> <dt>

<span id="_l"></span><span id="_L"></span>**/l**
</dt> <dd>

列出 SMIR 中的所有模組。

</dd> <dt>

<span id="_lc"></span><span id="_LC"></span>**/lc**
</dt> <dd>

在模組上執行本機語法檢查。

</dd> <dt>

<span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/ec** **\[<**_CommandModifier_*_>\]_*
</dt> <dd>

在模組上執行本機和外部檢查。

</dd> <dt>

<span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**\[ /a <**_CommandModifier_*_>\]_*
</dt> <dd>

執行本機和外部檢查，並將模組載入至 SMIR。

</dd> <dt>

<span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**\[ /sa <**_CommandModifier_*_>\]_*
</dt> <dd>

與 **/a** 相同，但以無訊息方式運作。

</dd> <dt>

<span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**\[ /g <**_CommandModifier_*_>\]_*
</dt> <dd>

產生 SMIR 的 mof 檔案，您稍後可以使用 MOF 編譯器將它載入至 WMI。 SNMP 類別提供者用來將類別動態提供給一或多個命名空間。 當您不知道受管理的 SNMP 裝置支援哪些 Mib 時，請使用此選項。 SNMP 類別提供者會在執行時間檢查裝置是否有此 MIB，並以動態方式將類別提供給命名空間。

</dd> <dt>

<span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**\[ /gc <**_CommandModifier_*_>\]_*
</dt> <dd>

產生靜態的 mof 檔案，該檔案可稍後載入至 WMI 作為特定命名空間的靜態類別。 當您知道受管理的 SNMP 裝置支援哪些 Mib 時，請使用此選項。 您可以藉由將命令的輸出導向至指定的檔案，來定義要產生的 mof 檔案。 請勿使用 with **/ext/o**。

</dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*CommandModifiers*>
</dt> <dd>

編譯器接受下列命令修飾詞。

<dl> <dt>

<span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**/i<**_目錄_*_>_*
</dt> <dd>

指定要搜尋的相依 MIB 模組目錄。 使用搭配 **/a**、 **/ec**、 **/g**、 **/gc** 和 **/sa**。 **/I** 選項可以出現在命令中多次;系統會依命令中指定的順序來搜尋目錄。

</dd> <dt>

<span id="_ch"></span><span id="_CH"></span>**/ch**
</dt> <dd>

產生 MOF 檔案標頭中的內容資訊，例如日期、時間、主機或使用者。 搭配 **/g** 和 **/gc** 使用。

</dd> <dt>

<span id="_t"></span><span id="_T"></span>**一起**
</dt> <dd>

產生 [SnmpNotification](snmpnotification.md) 類別。 搭配 **/a**、 **/g** 和 **/sa** 使用。

</dd> <dt>

<span id="_ext"></span><span id="_EXT"></span>**/ext**
</dt> <dd>

產生 [SnmpExtendedNotification](snmpextendednotification.md) 類別。 搭配 **/a**、 **/g** 和 **/sa** 使用。

</dd> <dt>

<span id="_t_o"></span><span id="_T_O"></span>**/t/o**
</dt> <dd>

只產生 [SnmpNotification](snmpnotification.md) 類別。 搭配 **/a**、 **/g** 和 **/sa** 使用。

</dd> <dt>

<span id="_ext_o"></span><span id="_EXT_O"></span>**/ext/o**
</dt> <dd>

只產生 [SnmpExtendedNotification](snmpextendednotification.md) 類別。 搭配 **/a**、 **/g** 和 **/sa** 使用。

</dd> <dt>

<span id="_s"></span><span id="_S"></span>**/s**
</dt> <dd>

不會對應 DESCRIPTION 子句的文字。 使用 **/a**、 **/g**、 **/gc** 和 **/sa**。 當您想要將儲存體需求降至最低時，請使用此選項。

</dd> <dt>

<span id="_auto"></span><span id="_AUTO"></span>**/auto**
</dt> <dd>

在完成 <*CommandArg*> 切換之前重建 MIB 查閱資料表。 使用 **/a**、 **/ec**、 **/g** 和 **/gc**。

</dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*RegistryArgs*>
</dt> <dd>

編譯器接受下列登錄引數。

<dl> <dt>

<span id="_pa"></span><span id="_PA"></span>**/pa**
</dt> <dd>

將指定的目錄新增至登錄。 預設值是目前的目錄。

</dd> <dt>

<span id="_pd"></span><span id="_PD"></span>**/pd**
</dt> <dd>

從登錄中刪除指定的目錄。 預設值是目前的目錄。

</dd> <dt>

<span id="_pl"></span><span id="_PL"></span>**/pl**
</dt> <dd>

列出登錄中的 MIB 查閱目錄。

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

重建整個 MIB 查閱資料表。

</dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*ModuleInfoArgs*>
</dt> <dd>

編譯器接受下列模組資訊引數。

<dl> <dt>

<span id="_n"></span><span id="_N"></span>**n**
</dt> <dd>

傳回指定模組的 ASN. 1 名稱。

</dd> <dt>

<span id="_ni"></span><span id="_NI"></span>**/ni**
</dt> <dd>

傳回輸入模組所參考之所有匯入模組的 asn.1 名稱。

</dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*HelpArgs*>
</dt> <dd>

編譯器接受下列說明引數。

<dl> <dt>

<span id="_h"></span><span id="_H"></span>**/h**
</dt> <dd>

顯示 SNMP 編譯器語法的說明。

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

顯示 SNMP 編譯器語法的說明。

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>備註

SNMP 資訊模組是以抽象語法標記法 (一)  (asn.1 的子集撰寫) 編譯器會執行下列功能：

-   從 SNMP 資訊模組載入資料。
-   在資訊模組上執行檢查操作。 例如，它會檢查本機語法，並且針對附屬模組中的資訊檢查外部參考。
-   從 SMIR 移除之前載入的所有資料，或從一個資訊模組移除載入的資料。
-   傳回指定檔案的 asn.1 模組名稱，或傳回指定檔案中所有匯入模組的 asn.1 模組名稱。
-   傳回 SMIR 中目前載入的所有 SNMP 資訊模組的 ASN.1 模組名稱。
-   會自動解決匯入的模組，而不需要使用者手動指定所需的模組。
-   執行不會產生任何輸出的無訊息載入模式，但是可以在安裝作業期間，用來將資料載入 SMIR。
-   將 SNMP 資訊模組中的資料輸出到 SMIR 中。
-   （選擇性）建立靜態或 SMIR MOF 檔案，其中包含資訊模組的輸出。

    如有必要，您可以將靜態的 mof 檔案載入至 WMI 命名空間。 SMIR mof 檔案包含類別應該位於其中的 SNMP 命名空間名稱。

## <a name="examples"></a>範例

下列範例會將 pra mof 檔案定義為 pra 的輸出。

``` syntax
smi2smir /m 3 /v1 /gc /pra.mib > pra.mof
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[SNMP 編譯器錯誤訊息](snmp-compiler-error-messages.md)
</dt> <dt>

[設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)
</dt> <dt>

[存取 SNMP 裝置](accessing-snmp-devices.md)
</dt> </dl>

 

 




