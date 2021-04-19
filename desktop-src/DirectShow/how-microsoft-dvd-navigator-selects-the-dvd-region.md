---
description: Microsoft DVD 導覽器如何選取 DVD 區域
ms.assetid: 407619c6-2d4b-4f7f-a861-42ee0f462ecd
title: Microsoft DVD 導覽器如何選取 DVD 區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f8a2898725ad187946b50e567f7daa7e72a9886
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "107000036"
---
# <a name="how-microsoft-dvd-navigator-selects-the-dvd-region"></a>Microsoft DVD 導覽器如何選取 DVD 區域

當您在電腦上播放 DVD 光碟時，Microsoft DVD 導覽器會使用下列演算法來判斷區域是否相符：

1.  DVD 導覽器會取得光碟區域、磁片磁碟機區域和解碼器區域。
2.  如果光碟區是「所有區域」，則 DVD 導覽器會播放光碟。
3.  如果光碟未標示為所有區域，則 DVD 導覽器會檢查解碼器是否有預設的區域。
4.  如果此解碼器具有預設的區域，而且不符合光碟區域，則 DVD 導覽器會傳回錯誤，指出無法在目前的 DVD 設定上播放光碟。  (Exit) 
5.  如果未設定解碼器區域，或與光碟區域相同，則 DVD 導覽器會檢查磁片磁碟機區域是否與光碟區域相同。
6.  如果磁片磁碟機區域符合光碟區域，則 DVD 導覽器會播放標題。
7.  否則，如果驅動程式區域不符合光碟區域，DVD 導覽器會叫用程式碼來變更磁片磁碟機的區域。 如果允許的區域變更數目已用盡，區域變更嘗試就會失敗，而且無法在該系統上播放標題。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 中的 DVD 區域變更支援](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



