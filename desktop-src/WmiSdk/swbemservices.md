---
description: 您可以使用 SWbemServices 物件的方法，對本機主機或遠端主機上的命名空間執行作業。 VBScript CreateObject 呼叫無法建立這個物件。
ms.assetid: 7fcfa404-2fe6-42e5-85ac-64536f6d2a44
ms.tgt_platform: multiple
title: 'SWbemServices 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices
- ISWbemServices
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4303b3226acc6d773ed35e77176e05e3a58c567d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983550"
---
# <a name="swbemservices-object"></a>SWbemServices 物件

您可以使用 **SWbemServices** 物件的方法，對本機主機或遠端主機上的命名空間執行作業。 VBScript **CreateObject** 呼叫無法建立這個物件。

## <a name="members"></a>成員

**SWbemServices** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**SWbemServices** 物件有這些方法。



| 方法                                                                         | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssociatorsOf**](swbemservices-associatorsof.md)                           | 透過一或多個關聯類別，取得與指定之資源相關聯之 managed 資源的實例。 您會提供原始端點的物件路徑，而 [**AssociatorsOf**](swbemservices-associatorsof.md) 會傳回相對端點的 managed 資源。 **AssociatorsOf** 方法會執行「ASSOCIATORS OF」 WQL 查詢所執行的相同函數。<br/>                                                                           |
| [**AssociatorsOfAsync**](swbemservices-associatorsofasync.md)                 | 以非同步方式傳回與指定物件相關聯)  (類別或實例的集合。<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| [**刪除**](swbemservices-delete.md)                                         | 刪除 managed 資源 (的實例，或從 CIM 存放庫) 的類別定義。<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**DeleteAsync**](swbemservices-deleteasync.md)                               | 以非同步方式刪除物件路徑中指定的類別或實例。<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ExecMethod**](swbemservices-execmethod.md)                                 | 提供另一種方法來執行 managed 資源類別定義所定義的方法。 主要是在指令碼語言不支援 out 參數的情況下使用。 例如，JScript 不支援 out 參數。<br/>                                                                                                                                                                                                                                            |
| [**ExecMethodAsync**](swbemservices-execmethodasync.md)                       | 以非同步方式執行方法提供者所匯出的方法。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ExecNotificationQuery**](swbemservices-execnotificationquery.md)           | 執行事件訂閱查詢以接收事件。 事件訂閱查詢是定義您想要監視的受管理環境變更的查詢。 發生變更時，WMI 基礎結構會提供事件，描述呼叫腳本的變更。<br/>                                                                                                                                                                                                        |
| [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) | 以非同步方式執行查詢以接收事件。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ExecQuery**](swbemservices-execquery.md)                                   | 執行查詢，以抓取受 WMI 管理之資源的實例集合 (或) 的類別定義。 [**ExecQuery**](swbemservices-execquery.md) 可以用來抓取已篩選的實例集合，這些實例符合您在傳遞至 **ExecQuery** 的查詢中定義的條件。<br/>                                                                                                                                                                                                           |
| [**ExecQueryAsync**](swbemservices-execqueryasync.md)                         | 以非同步方式執行查詢來取出物件。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Get**](swbemservices-get.md)                                               | 根據物件路徑，抓取 managed 資源 (或類別定義) 的單一實例。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**GetAsync**](swbemservices-getasync.md)                                     | 以物件路徑為基礎，以非同步方式抓取物件，也就是類別定義或實例。<br/>                                                                                                                                                                                                                                                                                                                                                                                |
| [**InstancesOf**](swbemservices-instancesof.md)                               | 根據類別名稱，抓取 managed 資源的所有實例。 根據預設， [**InstancesOf**](swbemservices-instancesof.md) 會執行深度抓取。 也就是說， **InstancesOf** 會抓取傳遞給方法之類別名稱所識別的資源實例，也會抓取所有子類別的所有實例， (在目標類別) 下定義。<br/>                                                                                       |
| [**InstancesOfAsync**](swbemservices-instancesofasync.md)                     | 根據使用者指定的選取準則，以非同步方式傳回指定之類別的實例。<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| [**ReferencesTo**](swbemservices-referencesto.md)                             | 傳回參考指定資源的所有關聯。 瞭解 [**ReferencesTo**](swbemservices-referencesto.md) 的最佳方式是將它與 [**AssociatorsOf**](swbemservices-associatorsof.md) 方法進行比較。 **AssociatorsOf** 會傳回位於關聯另一端的動態資源。 **ReferencesTo** 會傳回關聯本身。 **ReferencesTo** 方法會執行「WQL 查詢」所執行的相同函數。<br/> |
| [**ReferencesToAsync**](swbemservices-referencesto.md)                        | 以非同步方式傳回參考特定類別或實例的所有關聯類別或實例的集合。<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**SubclassesOf**](swbemservices-subclassesof.md)                             | 從 CIM 儲存機制抓取指定類別的所有子類別。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**SubclassesOfAsync**](swbemservices-subclassesofasync.md)                   | 以非同步方式傳回指定類別的子類別集合。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

### <a name="properties"></a>屬性

**SWbemServices** 物件具有這些屬性。



| 屬性                                                 | 存取類型          | Description                                                                          |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------|
| [**安全性\_**](swbemservices-security-.md)<br/> | 唯讀<br/> | 用來取得或設定 **SWbemServices** 物件的安全性設定。<br/> |



 

## <a name="remarks"></a>備註

可以在同步模式、非同步模式或半同步模式中呼叫方法。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

**概觀**

**SWbemServices** 有兩個主要角色。 首先， **SWbemServices** 物件代表與目的電腦上的 WMI 命名空間進行驗證的連接。 其次， **SWbemServices** 是您用來捕獲 WMI 管理資源的自動化物件。 您可以使用下列兩種方式之一取得 **SWbemServices** 物件的參考：

-   如同目前為止所呈現的大部分 WMI 腳本中所示範，您可以搭配使用 VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) 函數與 WMI 標記 "winmgmts："。 下列範例是最簡單的 WMI 連接形式。 此範例會連接到本機電腦上的預設命名空間 (通常是 "Root \\ CIMv2" ) ：

    `Set objSWbemServices = GetObject("winmgmts:")`

-   您也可以使用 [**wbemscripting.swbemlocator**](swbemlocator.md) 物件 [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) 方法來取得 **SWbemServices** 物件的參考。

取得 **SWbemServices** 物件的參考之後，您可以使用物件參考，以使用 **SWbemServices** 呼叫18個方法中的1個。 根據您呼叫的方法， **SWbemServices** 可以傳回三個不同的 WMI 腳本庫物件之一 ([**swbemobjectset 搭配使用**](swbemobjectset.md)、 [**SWbemObject**](swbemobject.md)或 [**SWbemEventSource**](swbemeventsource.md)) 。 知道每個方法所傳回的物件類型，將有助於您判斷腳本必須採取的下一個步驟。 例如，如果您取回 **swbemobjectset 搭配使用**，則必須列舉集合以存取集合中的每個 **SWbemObject** 。 如果您取回 **SWbemObject**，您可以立即存取物件方法和屬性，而不需要先列舉集合。

**作業模式**

**SWbemServices** 支援三種作業模式：同步、非同步和同步。

-   **同步**。 在同步模式中，除非 **SWbemServices** 方法完成，否則腳本會封鎖 (暫停) 。 您的腳本不只會等待，但在 WMI 抓取 managed 資源實例的情況下，WMI 會先在記憶體中建立整個 [**swbemobjectset 搭配使用**](swbemobjectset.md) ，然後再將第一個位元組的資料傳回給呼叫腳本。 這可能會對腳本效能以及執行腳本的電腦造成負面影響。 例如，以同步方式從 Windows 事件記錄檔中取出上千個事件可能需要很長的時間，而且會使用大量的記憶體。 基於這些理由，不建議使用同步作業，除非三個方法 ([**Delete**](swbemservices-delete.md)、 [**ExecMethod**](swbemservices-execmethod.md)和 [**Get**](swbemservices-get.md)) 預設為同步。 這些方法不會傳回大型資料集，因此不需要進行非半運算作業。
-   **非同步**。 在非同步模式中，您的腳本會呼叫其中九個非同步方法的其中一個，並立即傳回。 也就是說，只要呼叫非同步方法，您的腳本就會繼續執行下一行程式碼。 若要使用非同步方法，您的腳本必須先建立 [**SWbemSink**](swbemsink.md) 物件和特殊的副程式，稱為事件處理常式。 WMI 會執行非同步作業，並在作業完成時呼叫事件處理常式副程式來通知腳本。
-   **半同步**。 半同步模式是同步與非同步之間的折衷。 多工作業提供比同步作業更佳的效能，但不需要額外的知識和腳本步驟來處理非同步作業。 這是大部分 WMI 查詢的預設操作類型。

    在半同步模式中，您的腳本會呼叫六個數據抓取方法的其中一個，並立即傳回。 當您的腳本繼續執行時，WMI 會在背景中抓取受控資源。 當資源被抓取時，它們會透過 Swbemobjectset 搭配使用立即傳回到您的腳本。 您可以開始存取受管理的資源，而不需等候整個集合組合。

    當您使用的受控資源具有許多實例 (許多意義大於 1000) （例如 [**CIM \_ 資料檔案**](/windows/desktop/CIMWin32Prov/cim-datafile) 和 [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)）時，會對這項作業有一點注意。 警告是 WMI 處理 managed 資源實例的結果。 針對 managed 資源的每個實例，WMI 會建立並快取 [**SWbemObject**](swbemobject.md) 物件。 當受控資源有大量的實例時，實例抓取可以獨佔可用的資源，同時降低腳本和電腦的效能。

    若要解決此問題，您可以使用 **wbemFlagForwardOnly** 旗標來優化最半執行的方法呼叫。 **WbemFlagForwardOnly** 旗標（結合 **wbemFlagReturnImmediately** 旗標 (預設的最高值旗標) ）會告知 WMI 傳回順向 [**swbemobjectset 搭配使用**](swbemobjectset.md)，以消除大型資料集效能問題。 不過，使用 **wbemFlagForwardOnly** 旗標會產生成本。 只能列舉順向 **swbemobjectset 搭配使用** 一次。 存取順向 **swbemobjectset 搭配使用** 中的每個 [**SWbemObject**](swbemobject.md)之後，就會釋放配置給實例的記憶體。

除了 [**Delete**](swbemservices-delete.md)、 [**ExecMethod**](swbemservices-execmethod.md)、 [**Get**](swbemservices-get.md)和九個非同步方法之外，最半處理是預設和建議的作業模式。

**常用的方法**

系統管理腳本中最常用的方法是 [**InstancesOf**](swbemservices-instancesof.md)、 [**ExecQuery**](swbemservices-execquery.md)、 [**Get**](swbemservices-get.md)和 [**ExecNotificationQuery**](swbemservices-execnotificationquery.md)。 雖然通常會使用 **InstancesOf** ，但不一定是取得資訊 (的建議方式，雖然這是) 的最簡單方式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> <dt>

[呼叫方法](calling-a-method.md)
</dt> </dl>

 

