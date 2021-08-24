---
title: BITS 介面
description: 使用下列背景智慧型傳送服務 (位) 介面來傳送檔案，以及監視傳送佇列中的作業。
ms.assetid: 72668c9b-e6f3-4f3f-9d4b-50d930d1889d
ms.topic: article
ms.date: 01/08/2019
ms.openlocfilehash: 0edd4229e76a85767689427cfccd6cb38aa11c0e54345053ce10d1a99fc1fde8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529068"
---
# <a name="bits-interfaces"></a>BITS 介面

使用下列背景智慧型傳送服務 (位) 介面來 [傳送檔案，以及監視](using-bits.md) 傳送佇列中的作業。

| 介面 | 描述 |
|-|-|
| [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) | 用戶端會執行 [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) 介面，以接收作業已完成、已修改或發生錯誤的通知。 |
| [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) | 用戶端會執行 [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) 介面，以接收檔案已完成下載的通知。 |
| [**IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) | 用戶端會執行 [**IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) 介面，以接收檔範圍已完成下載的通知。 |
| [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) | 捕獲作業錯誤的詳細資料。 |
| [**IBackgroundCopyFile**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyfile) | 抓取作業中檔案傳輸要求的本機和遠端檔案名，以及其進度。 |
| [**IBackgroundCopyFile2**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyfile2) | 指定檔案的新遠端名稱，並抓取要下載的範圍清單。 |
| [**IBackgroundCopyFile3**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyfile3) | 驗證檔案，讓對等可以要求其內容並抓取暫存檔案的名稱。 |
| [**IBackgroundCopyFile4**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4) | 取得對等和源伺服器的下載統計資料。 |
| [**IBackgroundCopyFile5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5) | 提供 BackgroundCopyFile 屬性的泛型屬性 get 和 set 方法。 |
| [**IBackgroundCopyFile6**](/windows/desktop/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6) | 取得或設定 BITS 檔案傳輸的一般屬性。 |
| [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) | 將檔案加入至作業、設定作業的優先權層級、判斷工作的狀態，以及啟動和停止作業。 |
| [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) | 從上傳工作抓取回復資料、判斷回復資料傳送至用戶端的進度、要求命令列執行，並提供 proxy 和遠端伺服器的認證。 |
| [**IBackgroundCopyJob3**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3) | 下載檔案的範圍、變更遠端檔案名的前置詞，並使用檔案維護擁有者和 ACL 資訊。 |
| [**IBackgroundCopyJob4**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4) | 啟用對等快取、限制下載時間，以及檢查使用者 token 特性。 |
| [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) | 查詢或設定工作的數個選擇性行為。 |
| [**IBackgroundCopyJobHttpOptions**](/windows/desktop/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions) | 針對以憑證為基礎的用戶端驗證和自訂標頭，指定 HTTP 要求的用戶端憑證。 |
| [**IBackgroundCopyJobHttpOptions2**](/windows/desktop/api/Bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2) | 使用此介面來抓取及/或覆寫用於 BITS 傳送的 HTTP 方法。 |
| [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) | 建立傳送作業、抓取佇列中作業的列舉值物件，以及從佇列中取出個別的作業。 |
| [**IBitsPeer**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeer) | 取得鄰近地區中對等的相關資訊。 |
| [**IBitsPeerCacheAdministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) | 管理您可以從中下載內容的對等集區。 |
| [**IBitsPeerCacheRecord**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacherecord) | 取得快取中檔案的相關資訊。 |
| [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) | 將背景智慧型傳送服務 (BITS 的一組安全性權杖關聯和管理) 傳送作業。 |
| [**IEnumBackgroundCopyFiles**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyfiles) | 列舉作業中的檔案。 |
| [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) | 列舉傳送佇列中的作業。 |
| [**IEnumBitsPeerCacheRecords**](/windows/desktop/api/Bits3_0/nn-bits3_0-ienumbitspeercacherecords) | 列舉快取的記錄。 |
| [**IEnumBitsPeers**](/windows/desktop/api/Bits3_0/nn-bits3_0-ienumbitspeers) | 列舉位已探索到的對等清單。 |



 

 

 




