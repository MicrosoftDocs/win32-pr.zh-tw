---
description: 本節提供 WMI 類別和參考頁面資訊。
ms.assetid: 0110677a-bbba-42f7-8e59-55d83758f70a
ms.tgt_platform: multiple
title: WMI 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa764d39c1fb048e125898a1f7e6d5cadf7f127d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977846"
---
# <a name="wmi-classes"></a>WMI 類別

本節提供 WMI 類別和參考頁面資訊。 如需如何取出類別或實例資料的詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。 下列清單列出、描述和提供特定 WMI 類別資訊的連結。 如需使用 WMI 類別取得各種作業系統和硬體資料的詳細資訊和腳本程式碼範例，請參閱 [腳本和應用程式的 wmi](wmi-tasks-for-scripts-and-applications.md)工作。 如需 c + + 的範例，請參閱 [WMI c + + 應用程式範例](wmi-c---application-examples.md)。 [連接至遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md) 會顯示如何取得遠端資料。 您也可以使用 PowerShell 來存取 WMI 物件;如需包含 PowerShell 程式碼範例的 WMI 類別清單，請參閱 [這裡](https://msdn.microsoft.com/library/tags-cloud.aspx?tag=powershell+code+wmi)。



| 區段                                                    | 描述                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [WMI 系統類別](wmi-system-classes.md)               | 預先定義的類別，包含在 Windows Management Instrumentation (WMI) 核心的每個命名空間中。 您可以辨識 WMI 系統類別，因為名稱的開頭是雙底線 (\_ \_) 。 這些類別提供 WMI 的許多基本功能。 WMI 系統類別的用途與 SQL server 中的系統資料表類似。 |
| [MSFT 類別](msft-classes.md)                           | 其他 Microsoft 類別，提供運算元種作業系統功能的方法，例如遠端事件和原則延伸。 [Wmi 疑難排解](wmi-troubleshooting.md)類別是 MSFT 類別，可提供 WMI 作業的相關資料。                                                                                               |
| [CIM 類別](cimclas.md)                                 | [*通用訊息模型 (CIM)*](gloss-c.md) 架構類別。 如果您想要撰寫自己的 WMI 類別，則可以繼承自其中一或多個類別。 WMI [Win32 類別](/windows/desktop/CIMWin32Prov/win32-provider) 繼承自 CIM 類別。                                                                          |
| [標準取用者類別](standard-consumer-classes.md) | 一組 WMI 事件取用者，這些取用者會在收到任意事件時觸發動作。 如需詳細資訊，請參閱 [監視事件](monitoring-events.md)。                                                                                                                                                                                               |



 

## <a name="wmi-class-scripting-center-code-examples"></a>WMI 類別腳本中心程式碼範例

下列腳本中心程式碼範例會跨多個命名空間影響多個 WMI 類別。



| 連結                                                                                                                                      | 描述                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [GUI WMI Explorer 和 WMI 方法說明產生器](https://Gallery.TechNet.Microsoft.Com/scriptcenter/89c759b7-20b4-49e8-98a8-3c8fbdb2dd69) | 提供 GUI WMI Explorer 和 WMI 方法說明產生器的範例腳本。                                                                                                                                                        |
| [WMI Explorer 搜尋 WMI 命名空間](https://Gallery.TechNet.Microsoft.Com/scriptcenter/WMI-Explorer-Search-WMI-cd87e309)                 | 可讓使用者在指定的電腦上搜尋所有可用命名空間中的類別。 此範例是 GUI WMI Explorer 範例的命令列新版，可視為 Get-WmiObject 清單的延伸模組。 |
| [Arposh Windows 系統管理工具](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Arposh-Windows-System-a1beb102)            | AWSA 是由系統管理員所建立。 針對 Windows 問題進行疑難排解需要大量的工具和知識。 AWSA 會將這些工具結合在一個中央位置，並新增額外的功能。       |



 

## <a name="naming-conventions-for-wmi-classes-and-properties"></a>WMI 類別和屬性的命名慣例

屬性名稱必須符合分散式管理工作推動力 (DTMF) 所定義的受控物件格式 (MOF) 語法。 初始識別碼字元必須是來自字母 a 到 z，而底線字元 (\_) 。 所有其他字元都必須來自字母 a 到 z、底線字元和數位0到9。 如需詳細資訊，請參閱 [CIM 規格2.2 版](https://www.dmtf.org/standards/cim)的 Unicode 使用方式一節。

SQL 保留字不應該用在類別和屬性名稱中。 如需 SQL 保留字和詳細資訊的完整清單，請參閱 [CIM 規格2.2 版](https://www.dmtf.org/standards/cim)的指導方針一節。

## <a name="document-conventions-for-a-wmi-class-reference-page"></a>WMI 類別參考頁面的檔慣例

本節將識別及描述 WMI 類別參考頁面的檔慣例。

一般參考頁面包含語法區塊、方法資料表和屬性清單。

-   語法區塊

    MOF 程式碼的簡化版本，包含類別名稱、父類別 (（如果有任何) ）和類別屬性（以字母順序表示）與資料類型。

-   方法資料表

    如果類別具有方法，則方法會列在緊接在語法區塊後面的資料表中。 每個已執行的方法都會連結到參考頁面。

-   屬性清單

    每個類別屬性都會以資料類型、存取類型 (唯讀或讀取/寫入) 、限定詞，以及屬性的描述來列出。

## <a name="syntax-block"></a>語法區塊

``` syntax
class Win32_xyz : CIM_xyz 
{
  uint16 abc  ;
  string def  ;
};
```

## <a name="methods-table"></a>方法資料表



| Win32 \_ xyz 方法 | Description                                |
|--------------------|--------------------------------------------|
| *SomeMethod*       | 方法用途的簡短描述。 |



 

## <a name="properties-list"></a>屬性清單

<dl> <dt>

<span id="abc"></span><span id="ABC"></span>Abc
</dt> <dd>

資料類型： **uint16**

存取類型：顯示您是否擁有這個屬性的讀取/寫入或唯讀存取權。

限定詞：如果存在，則會顯示內容的限定詞。 例如， **Key**、 **Override**。

描述屬性，並提供屬性的繼承資訊。 例如，這個屬性繼承自 **CIM \_* xyz * * *。 如果 Microsoft 提供該類別的執行，則會有父類別的連結。 但是，無法使用 CIM 類別。

</dd> <dt>

<span id="def"></span><span id="DEF"></span>Def
</dt> <dd>

資料類型： **字串**

存取類型：唯讀

屬性的描述。

</dd> </dl>

## <a name="remarks"></a>備註

提供類別的詳細資訊（如果適用）。 也提供衍生資訊（如果適用）。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 參考](wmi-reference.md)
</dt> </dl>

 

 
