---
title: 與 IMAPI.EXE 互動
description: 下列步驟說明應用程式與 IMAPI.EXE 之間的一般互動。
ms.assetid: e57a86c4-7e27-40cf-a9c1-081b3f20d9d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab97d1a9d76d1e82dab64fb777ef5207d3d47560b2a889981c698ab78e3622b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726988"
---
# <a name="interacting-with-imapi"></a>與 IMAPI.EXE 互動

下列步驟說明應用程式與 IMAPI.EXE 之間的一般互動。

1.  使用 **CoCreateInstance**、從匯入的智慧型指標 (建立 **MSDiscMasterObj** 的實例，然後) 並要求 [**IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster)介面。
2.  藉由呼叫 [**IDiscMaster：： Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open)來取得 imapi.exe 的存取權。 如果此呼叫成功，則應用程式具有 **MSDiscMasterObj** 中所執行之所有介面和方法的完整存取權。
3.  使用 [**EnumDiscMasterFormats**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-enumdiscmasterformats)取出光碟主要格式列舉值。 列舉光碟主機物件所支援的一組格式，然後選取使用中的格式。 從列舉值傳回的格式是 [**IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) 和 [**IRedbookDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster)介面的 iid。
4.  使用 [**EnumDiscRecorders**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-enumdiscrecorders)取出光碟錄製器列舉值。 列舉支援的光碟機清單 (特定于現用格式) ，然後選取使用中的錄製器。 [**IDiscRecorder**](/windows/desktop/api/Imapi/nn-imapi-idiscrecorder)介面代表實體裝置。
5.  使用 [**IDiscMaster：:P rogressadvise**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-progressadvise) 來註冊進度回呼。
6.  使用所選格式的介面來建立內容。 內容會以累加的方式建立，因此可依片段將追蹤或資料夾內容新增到光碟片。 建立此內容的程式稱為 *暫存映射*。 無法以累加方式刪除暫存映射的內容 (您無法移除已新增) 的播放軌，但可以清除暫存影像的內容，讓暫存可以再次啟動。 使用 [**IDiscMaster：： ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) 重新開機暫存。

* * 適用于音訊： * *

1.  使用 [**IRedbookDiscMaster：： CreateAudioTrack**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-createaudiotrack) 指出正在光碟上啟動新的音訊播放軌。
2.  使用 [**IRedbookDiscMaster：： AddAudioTrackBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-addaudiotrackblocks) 將原始音訊資料新增至曲目。應用程式可以使用 [**GetAvailableAudioTrackBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-getavailableaudiotrackblocks)、 [**GetTotalAudioBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-gettotalaudioblocks)和 [**GetUsedAudioBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-getusedaudioblocks) 來取得統計資訊。
3.  使用 [**IRedbookDiscMaster：： CloseAudioTrack**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-closeaudiotrack) 關閉音訊播放軌。
4.  重複步驟1-3，直到空間不足或已寫入所有音訊曲目為止。

* * 表示資料： * *

1.  使用 [**IJolietDiscMaster：： AddData**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-adddata) 將資料夾的內容新增至映射。 資料夾內的專案會放在影像檔案的根目錄中。 使用 [**GetTotalDataBlocks**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-gettotaldatablocks) 和 [**GetUsedDataBlocks**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-getuseddatablocks) 來取得統計資訊。
2.  重複上述步驟，直到空間不足或已新增所有資料為止。

* * 適用于所有光碟： * *

1.  使用 [**IDiscMaster：： RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) 來記錄光碟。
2.  使用 [**IDiscMaster：： close**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-close)關閉 imapi.exe 會話。 關閉會話會清除隱藏的光碟內容。

 

 




