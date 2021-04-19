---
description: 深入瞭解：完整的服務範例
ms.assetid: a3aeea9b-09c0-4834-892a-c378b67402f4
title: 完整的服務範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb87ebfef3f964eacee66be94a4b5291c335d0d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980453"
---
# <a name="the-complete-service-sample"></a>完整的服務範例

本節中的主題會形成完整的服務範例：

-   [Sample.mc](sample-mc.md) (包含錯誤訊息) 
-   [.Svc .cpp](svc-cpp.md) (包含服務程式代碼) 
-   [SvcConfig .cpp](svcconfig-cpp.md) (包含服務設定程式碼) 
-   [SvcControl .cpp](svccontrol-cpp.md) (包含服務控制程式代碼) 

## <a name="building-the-service"></a>建置服務

下列程式描述如何建立服務並註冊事件訊息 DLL。

**若要建立服務並註冊事件訊息 DLL**

1.  使用下列步驟，從 Sample.mc 建立訊息 DLL：
    1.  **mc-U sample.mc**
    2.  **rc-r 範例 .rc**
    3.  **程式庫-noentry -out:sample.dll 範例 .res**
2.  分別從 .Svc、SvcConfig .cpp 和 SvcControl 建立 Svc.exe、SvcConfig.exe 和 SvcControl.exe。
3.  建立登錄機碼 **HKEY \_ 本機 \_ 電腦 \\ 系統 \\ CurrentControlSet \\ 服務 \\ EventLog \\ 應用程式 \\ SvcName** ，並將下列登錄值新增至此索引鍵。

    | 值                              | 類型       | Description                                                                                                        |
    |------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------|
    | **EventMessageFile**  = *dll \_ 路徑* | REG \_ SZ    | 僅含資源的 DLL 路徑，其中包含服務可寫入事件記錄檔中的字串。               |
    | **TypesSupported** = 0x00000007    | REG \_ DWORD | 指定支援的事件種類的位元遮罩。 值0x000000007 表示支援所有類型。 |

    

     

## <a name="testing-the-service"></a>測試服務

下列程式說明如何測試服務。

**若要測試服務**

1.  在主控台中，啟動 [ **服務** ] 應用程式。  (在下列步驟中，在執行修改 **服務** 應用程式中資訊的命令之後，使用 F5 鍵重新整理顯示。 ) 
2.  執行下列命令以安裝服務：

    **svc 安裝**

    如果作業成功，服務就會將「服務安裝成功」寫入主控台，否則會傳回錯誤訊息。

    如果服務安裝成功，服務就會顯示在 [ **服務** ] 應用程式中。 請注意，[ **名稱** ] 設定為 "SvcName"、 **描述** 和 **狀態** 為空白，而 [ **啟動類型** ] 設定為 [手動]。

3.  執行下列命令來啟動服務：

    **svccontrol 開始 SvcName**

    如果作業成功，服務控制程式會寫入「服務開始擱置中 ...」然後「服務已成功啟動」至主控台。 否則，程式會將錯誤訊息寫入主控台。

    如果服務成功啟動，則 **狀態** 會設定為「已啟動」。 [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona)函式中的程式碼是由 SCM 執行。 如果發生錯誤，服務會將錯誤訊息寫入至事件記錄檔。 此訊息包含失敗的函式名稱，以及失敗時傳回的錯誤碼。

4.  執行下列命令以更新服務描述：

    **svcconfig 描述 SvcName**

    如果作業成功，服務設定程式會將「服務描述更新成功」寫入主控台，否則會傳回錯誤訊息。

    如果更新成功， **描述** 會設定為「這是測試描述」。

5.  執行下列命令來查詢服務設定：

    **svcconfig 查詢 SvcName**

    如果作業成功，服務設定程式會將服務設定資訊寫入主控台，否則會傳回錯誤訊息。

6.  執行下列命令來變更服務 DACL：

    **svccontrol dacl SvcName**

    如果作業成功，服務設定程式會將「服務 DACL 更新成功」寫入主控台，否則會傳回錯誤訊息。

7.  執行下列命令以停用服務：

    **svcconfig 停用 SvcName**

    如果作業成功，服務設定程式會將「服務已成功停用」寫入主控台，否則會傳回錯誤訊息。

    如果服務已成功停用， **啟動類型** 會設定為「已停用」。

8.  執行下列命令以啟用服務：

    **svcconfig 啟用 SvcName**

    如果作業成功，服務設定程式會將「已成功啟用服務」寫入主控台，否則會傳回錯誤訊息。

    如果成功啟用服務，[ **啟動類型** ] 設定為 [手動]。

9.  執行下列命令來停止服務：

    **svccontrol 停止 SvcName**

    如果作業成功，服務控制程式會將 "Service stop pending ..." 寫入然後「服務已成功停止」至主控台。 否則，程式會將錯誤訊息寫入主控台。

    如果服務成功停止， **狀態** 會是空白。

    如果服務無法停止，服務控制程式會將錯誤訊息寫入至事件記錄檔，其中包含失敗的函式名稱，以及失敗時傳回的錯誤碼。

10. 執行下列命令來刪除服務：

    **svcconfig 刪除 SvcName**

    如果作業成功，服務設定程式會將「服務刪除成功」寫入主控台，否則會傳回錯誤訊息。

    如果成功刪除服務， **服務** 應用程式就不會再顯示該服務。  (請注意，如果您嘗試刪除未停止的服務，該作業會成功，但 [ **啟動類型** ] 設定為 [已停用]，而在系統重新開機時或使用工作管理員終止服務時，會刪除服務專案。 ) 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用服務](using-services.md)
</dt> </dl>

 

 
