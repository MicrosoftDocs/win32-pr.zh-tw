---
title: 提供者總覽
description: 提供者應用程式的概念總覽。
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: c6905d6d2d52fd30b8950682c45c9d3bd0fc13281fc0f1d3120cba1b168012d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127958"
---
# <a name="provider-overview"></a>提供者總覽

提供者是一種使用者模式應用程式，可維護及瞭解支援資料存放區。  此提供者會實 ProjFS 回呼，並使用 ProjFS API 將此資料存放區投射到檔案系統中，並以檔案和目錄的形式呈現給使用者。  提供者的備份存放區可以在使用者的系統本機上進行，也可能位於遠端。

## <a name="data-projection"></a>資料投射

提供者所擁有的檔案系統部分（投射其資料的位置）根目錄為名為「虛擬化根」的目錄。  當提供者想要開始投射其資料時，它會啟動「虛擬化實例」，這是一種物件，可管理位於特定虛擬化根目錄下之檔案和目錄集合的提供者與 ProjFS 之間的通訊。  在使用者本機未建立之虛擬化根項目的任何檔案和目錄都是由提供者透過 ProjFS API 具體化。  這些專案會以虛擬檔案和目錄的形式啟動，這表示它們不存在於使用者的本機儲存裝置上，而是藉由 ProjFS 插入列舉結果中。  開啟和讀取專案時，ProjFS 會叫用提供者所執行的回呼來要求資料，而且提供者會使用 ProjFS Api，將該資料傳送至快取的本機儲存體，以供後續存取。  如果使用者對支援資料存放區的觀點需要變更，例如，如果資料存放區的內容已變更，則提供者可以使用 ProjFS Api 來更新或刪除本機專案，以反映資料存放區的新觀點。

## <a name="callback-return-codes"></a>回呼傳回碼

每個回呼都會列出該回呼特定的一些可能傳回值。  除了針對指定回呼列出的傳回值之外，回呼也可能會傳回某些其他錯誤碼。  這是回呼可能會傳回的完整錯誤碼清單：

| 錯誤碼                                    | 意義
|-----------------------------------------------|--------
| S_OK                                          | 操作成功
| E_OUTOFMEMORY                                 | 無法配置所需的記憶體。
| HRESULT_FROM_WIN32 (ERROR_IO_PENDING)           | 提供者希望稍後完成此作業。
| HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) | 傳遞給回呼的緩衝區太小。
| HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)      | 檔案不存在於提供者的備份存放區中。
| HRESULT_FROM_WIN32 (ERROR_INVALID_PARAMETER)    | 回呼引數無效。  例如，列舉識別碼不會對應至使用中的列舉會話。
| HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)       | 提供者希望防止作業（例如重新命名或刪除）發生。

回呼也可能會傳回任何可能從呼叫 ProjFS Api 收到的錯誤。
如果回呼傳回的錯誤碼不在上述清單中，或不是來自 ProjFS API，則 ProjFS 會將它以 STATUS_INTERNAL_ERROR 的方式傳回檔案系統。
