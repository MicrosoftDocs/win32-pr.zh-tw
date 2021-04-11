---
description: 列舉通常會使用大量的系統資源。
ms.assetid: 4163e6c2-4ee3-4906-b297-618509666c90
ms.tgt_platform: multiple
title: 改善列舉效能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2554e9e1df2f2ece58f5703d6099d84acbe01c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193867"
---
# <a name="improving-enumeration-performance"></a>改善列舉效能

列舉通常會使用大量的系統資源。 因此，如果您打算在大型群組上執行列舉，您應該嘗試將 WMI 列舉程式優化。 腳本也可以使用查詢，以避免「針對每個 ...」作業使用大型集合的效能降低。 如需詳細資訊，請參閱 [查詢 WMI](querying-wmi.md)。

下列程式描述如何改善列舉效能。

**改善列舉效能**

1.  將 *lFlags* 參數設定為允許在每次傳遞時從 WMI 中捨棄每個專案的列舉值，以允許最半傳回資料。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

    下列 c + + 程式碼範例示範如何使用 **WBEM \_ 旗 \_ \_** 標，傳回立即和 **WBEM 旗標順 \_ \_ 向 \_** 旗標。

    `WBEM_FLAG_RETURN_IMMEDIATE | WBEM_FLAG_FORWARD_ONLY`

    在 VBScript 或 Visual Basic 中，請使用 [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)中的腳本旗標 **WbemFlagReturnImmediately** 和 **WbemFlagForwardOnly** 。 這些旗標的合併值是十進位48。

    腳本和參數旗標會導致下列行為：

    -   WBEM 旗標會傳回 **\_ \_ \_ 立即** 或 **wbemFlagReturnImmediately** 旗標要求的最半行為。 建立列舉值的呼叫會立即傳回。 然後，您可以開始遍歷您收到的物件集。
    -   **WBEM \_ 旗標 \_ \_ 僅向前** 旗標或 **wbemFlagForwardOnly** 旗標會要求您無法倒轉的列舉值。 也就是說，在您查看物件之後，WMI 可以釋放物件。

    在列舉很大且應用程式非常快速的情況下，使用順向列舉值搭配半同步處理可讓 WMI 保持較少的物件，進而大幅增加回應時間和記憶體效能。

    下列 VBScript 程式碼範例示範如何使用合併的 **wbemFlagReturnImmediately** 和 **wbemFlagForwardOnly** 旗標來進行呼叫，以從事件記錄檔取得事件的集合。

    ```VB
    Set Events = GetObject("winmgmts:").ExecQuery _
         ("SELECT * FROM Win32_NTLogEvent " _
          & "WHERE Logfile = 'System'",,48)
    ```

    

2.  可能的話，請避免在 c + + 或 [**SWbemServices InstancesOf**](swbemservices-instancesof.md)中使用 [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) ，而改為使用 **ExecQuery**。

    **ExecQuery** 方法會使用資料庫技術來查詢 wmi，而 [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)或 [**SWbemServices**](swbemservices-instancesof.md)則會列舉 wmi 物件。 具體而言， **ExecQuery** 可以要求列舉方法無法進行的特定資料子集。

    由於某些提供者沒有查詢功能，因此 WMI 提供「後篩選」功能，可讓 WMI 捨棄未滿足查詢規格的實例。 特定提供者是否可利用這項功能，是由提供者的作者所決定。

3.  使用不同的查詢進行實驗，以判斷可提供最佳效能的方式。

    例如，WMI 很少會有效率地使用 Prop1 格式的 **WHERE** 子句來處理查詢 < "x"。 相反地，WMI 通常會有效率地處理 KeyProp1 = "x" 形式的查詢。

如需詳細資訊，請參閱 [列舉 WMI](enumerating-wmi.md)。

 

 



