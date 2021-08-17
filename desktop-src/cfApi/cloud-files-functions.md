---
description: 下列函式用於建立和維護預留位置檔案和目錄。
ms.assetid: 68B667E2-E8C6-41F9-A0E2-C8CDF60D6472
title: 雲端篩選函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9793306aa8715e6de30c228094b8eaf6d984ca4f752751619063ae84115ec4ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737480"
---
# <a name="cloud-filter-functions"></a>雲端篩選函數

下列函式用於建立和維護預留位置檔案和目錄。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                  | 描述                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CfCloseHandle**](/windows/desktop/api/cfapi/nf-cfapi-cfclosehandle)<br/>                                                 | 關閉 [**CfOpenFileWithOplock**](/windows/desktop/api/cfapi/nf-cfapi-cfopenfilewithoplock)所傳回的檔案或目錄控制碼。 這不應該與標準 Win32 檔案控制代碼搭配使用，只能在 CfApi 中使用的控制碼上使用。<br/> |
| [**CfConnectSyncRoot**](/windows/desktop/api/cfapi/nf-cfapi-cfconnectsyncroot)<br/>                                         | 起始同步處理提供者與同步篩選 API 之間的雙向通訊。<br/>                                                                                                                   |
| [**CfConvertToPlaceholder**](/windows/desktop/api/cfapi/nf-cfapi-cfconverttoplaceholder)<br/>                               | 將一般檔案/目錄轉換成預留位置檔案/目錄。<br/>                                                                                                                                         |
| [**CfCreatePlaceholders**](/windows/desktop/api/cfapi/nf-cfapi-cfcreateplaceholders)<br/>                                   | 在同步根樹狀目錄下建立一或多個新的預留位置檔案或目錄。<br/>                                                                                                                          |
| [**CfDisconnectSyncRoot**](/windows/desktop/api/cfapi/nf-cfapi-cfdisconnectsyncroot)<br/>                                   | 中斷 [**CfConnectSyncRoot**](/windows/desktop/api/cfapi/nf-cfapi-cfconnectsyncroot)所建立的通道連線。<br/>                                                                                                       |
| [**CfExecute**](/windows/desktop/api/cfapi/nf-cfapi-cfexecute)<br/>                                                         | 所有以連接索引鍵為基礎的預留位置作業的主要進入點。 它是供同步處理提供者用來回應平臺的各種回呼。<br/>                                 |
| [**CfGetCorrelationVector**](/windows/desktop/api/cfapi/nf-cfapi-cfgetcorrelationvector)<br/>                               | 允許同步處理提供者針對指定的預留位置檔案查詢目前的相互關聯向量。<br/>                                                                                                            |
| [**CfGetPlaceholderInfo**](/windows/desktop/api/cfapi/nf-cfapi-cfgetplaceholderinfo)<br/>                                   | 取得預留位置檔案或資料夾的各種特性。<br/>                                                                                                                                             |
| [**CfGetPlaceholderRangeInfo**](/windows/desktop/api/cfapi/nf-cfapi-cfgetplaceholderrangeinfo)<br/>                         | 取得預留位置檔案或資料夾的範圍資訊。<br/>                                                                                                                                                |
| [**CfGetPlaceholderStateFromAttributeTag**](/windows/desktop/api/cfapi/nf-cfapi-cfgetplaceholderstatefromattributetag)<br/> | 根據檔案的 *FileAttributes* 和 *ReparseTag* 值，取得一組預留位置狀態。<br/>                                                                                                       |
| [**CfGetPlaceholderStateFromFileInfo**](/windows/desktop/api/cfapi/nf-cfapi-cfgetplaceholderstatefromfileinfo)<br/>         | 根據檔案的各種資訊，取得一組預留位置狀態。<br/>                                                                                                                            |
| [**CfGetPlaceholderStateFromFindData**](/windows/desktop/api/cfapi/nf-cfapi-cfgetplaceholderstatefromfinddata)<br/>         | 根據 WIN32 \_ 尋找資料結構取得一組預留位置狀態 \_ 。<br/>                                                                                                                                |
| [**CfGetPlatformInfo**](/windows/desktop/api/cfapi/nf-cfapi-cfgetplatforminfo)<br/>                                         | 取得平臺版本資訊。<br/>                                                                                                                                                                    |
| [**CfGetSyncRootInfoByHandle**](/windows/desktop/api/cfapi/nf-cfapi-cfgetsyncrootinfobyhandle)<br/>                         | 取得同步處理根的各種特性，其中包含檔案控制代碼所指定的指定檔案。<br/>                                                                                                         |
| [**CfGetSyncRootInfoByPath**](/windows/desktop/api/cfapi/nf-cfapi-cfgetsyncrootinfobypath)<br/>                             | 取得在同步根目錄下提供檔案的各種同步根資訊。<br/>                                                                                                                                      |
| [**CfGetTransferKey**](/windows/desktop/api/cfapi/nf-cfapi-cfgettransferkey)<br/>                                           | 起始將資料傳輸到預留位置檔案或資料夾。<br/>                                                                                                                                           |
| [**CfGetWin32HandleFromProtectedHandle**](/windows/desktop/api/cfapi/nf-cfapi-cfgetwin32handlefromprotectedhandle)<br/>     | 將受保護的控制碼轉換成 Win32 控制碼，讓它可以與所有以控制碼為基礎的 Win32 Api 搭配使用。 <br/>                                                                                                   |
| [**CfHydratePlaceholder**](/windows/desktop/api/cfapi/nf-cfapi-cfhydrateplaceholder)<br/>                                   | 確定指定的位元組範圍是否存在於磁片上的預留位置中，以產生預留位置檔案。 這僅適用于檔案。<br/>                                                                |
| [**CfOpenFileWithOplock**](/windows/desktop/api/cfapi/nf-cfapi-cfopenfilewithoplock)<br/>                                   | 針對一般和預留位置檔案，開啟檔案或目錄 (的非同步不透明控制碼) 並根據開啟的旗標，在其上設定適當的 oplock。<br/>                                             |
| [**CfQuerySyncProviderStatus**](/windows/desktop/api/cfapi/nf-cfapi-cfquerysyncproviderstatus)<br/>                         | 查詢同步處理提供者，以取得提供者的狀態。<br/>                                                                                                                                                |
| [**CfReferenceProtectedHandle**](/windows/desktop/api/cfapi/nf-cfapi-cfreferenceprotectedhandle)<br/>                       | 允許呼叫者參考受保護的 Win32 控制碼控制碼，該控制碼可搭配非 CfApi 的 Win32 Api 使用。 <br/>                                                                                         |
| [**CfRegisterSyncRoot**](/windows/desktop/api/cfapi/nf-cfapi-cfregistersyncroot)<br/>                                       | 執行單次同步根目錄註冊。<br/>                                                                                                                                                               |
| [**CfReleaseProtectedHandle**](/windows/desktop/api/cfapi/nf-cfapi-cfreleaseprotectedhandle)<br/>                           | 釋放 [**CfReferenceProtectedHandle**](/windows/desktop/api/cfapi/nf-cfapi-cfreferenceprotectedhandle)所參考的受保護控制碼。<br/>                                                                                          |
| [**CfReleaseTransferKey**](/windows/desktop/api/cfapi/nf-cfapi-cfreleasetransferkey)<br/>                                   | 釋放 [**CfGetTransferKey**](/windows/desktop/api/cfapi/nf-cfapi-cfgettransferkey)取得的傳輸金鑰。<br/>                                                                                                                    |
| [**CfReportProviderProgress**](/windows/desktop/api/cfapi/nf-cfapi-cfreportproviderprogress)<br/>                           | 允許同步處理提供者報告頻外的進度。<br/>                                                                                                                                                    |
| [**CfReportSyncStatus**](/windows/desktop/api/cfapi/nf-cfapi-cfreportsyncstatus)<br/>                                       | 允許同步處理提供者在指定的同步根上通知其狀態的平臺，而不需要先與 [**CfConnectSyncRoot**](/windows/desktop/api/cfapi/nf-cfapi-cfconnectsyncroot) 的呼叫進行連接。 <br/>                 |
| [**CfRevertPlaceholder**](/windows/desktop/api/cfapi/nf-cfapi-cfrevertplaceholder)<br/>                                     | 將預留位置還原回一般檔案，去除所有的特殊特性，例如重新分析標記、檔案識別等等。<br/>                                                                 |
| [**CfSetCorrelationVector**](/windows/desktop/api/cfapi/nf-cfapi-cfsetcorrelationvector)<br/>                               | 允許同步處理提供者在預留位置檔案上指示平臺針對遙測用途使用特定的相互關聯向量。 這是選擇性的。<br/>                                                      |
| [**CfSetInSyncState**](/windows/desktop/api/cfapi/nf-cfapi-cfsetinsyncstate)<br/>                                           | 設定預留位置檔案或資料夾的同步處理狀態。<br/>                                                                                                                                                  |
| [**CfSetPinState**](/windows/desktop/api/cfapi/nf-cfapi-cfsetpinstate)<br/>                                                 | 這會設定預留位置的釘選狀態，用來代表使用者的意圖。 任何應用程式不只 (同步處理提供者) 都可以呼叫這個函數。<br/>                                                         |
| [**CfUnregisterSyncRoot**](/windows/desktop/api/cfapi/nf-cfapi-cfunregistersyncroot)<br/>                                   | 取消註冊先前註冊的同步根。<br/>                                                                                                                                                            |
| [**CfUpdatePlaceholder**](/windows/desktop/api/cfapi/nf-cfapi-cfupdateplaceholder)<br/>                                     | 更新預留位置檔案或目錄的特性。<br/>                                                                                                                                             |
| [**CfUpdateSyncProviderStatus**](/windows/desktop/api/cfapi/nf-cfapi-cfupdatesyncproviderstatus)<br/>                       | 更新同步處理提供者的目前狀態。<br/>                                                                                                                                                          |



 

 

