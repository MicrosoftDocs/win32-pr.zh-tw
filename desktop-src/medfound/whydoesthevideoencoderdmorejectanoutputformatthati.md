---
description: 當我從相同物件取出格式時，為什麼影片編碼器會拒絕我嘗試設定的輸出格式？
ms.assetid: f0747450-d224-423a-a9f1-04580df8a17e
title: 當我從相同物件取出格式時，為什麼影片編碼器會拒絕我嘗試設定的輸出格式？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2e744285140df13a9aa251983ab801033c481d1452029c955ee3a39235fcea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112888"
---
# <a name="why-does-the-video-encoder-reject-an-output-format-that-i-try-to-set-when-i-retrieved-the-format-from-the-same-object"></a>當我從相同物件取出格式時，為什麼影片編碼器會拒絕我嘗試設定的輸出格式？

與音訊編碼器輸出類型不同的是，影片編碼器所列舉的支援輸出不會如傳遞完成。 您必須在 **VIDEOINFOHEADER** 結構的 **dwBitrate** 成員中設定資料流程的位元速率，以符合針對 [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)屬性所設定的值。

當所有選項都設定為您想要的方式之後，您必須抓取編解碼器私用資料，並將它附加至 **VIDEOINFOHEADER** 結構。 如需詳細資訊，請參閱 [使用影片編解碼器私用資料](usingvideocodecprivatedata.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[常見問題集](frequentlyaskedquestions.md)
</dt> </dl>

 

 



