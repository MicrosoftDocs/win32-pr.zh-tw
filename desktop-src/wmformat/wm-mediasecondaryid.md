---
title: WM/MediaClassSecondaryID
description: WM/MediaClassSecondaryID 屬性包含次要媒體類別的 GUID。
ms.assetid: 3d1429bc-f168-4b25-9d26-c1c28b852160
keywords:
- WM/MediaClassSecondaryID windows Media 格式
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5923ff0ff0545f1feb769973f2528bd82e351e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373257"
---
# <a name="wmmediaclasssecondaryid"></a>WM/MediaClassSecondaryID

**WM/MediaClassSecondaryID** 屬性包含次要媒體類別的 GUID。

## <a name="global-constant"></a>全域常數

g \_ wszWMMediaClassSecondaryID

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ GUID**

## <a name="remarks"></a>備註

這個屬性應該設定為下表中的其中一個值。



| 次要類別 GUID                   | Description                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "E0236BEB-C281-4EDE-A36D-7AF76A3D45B5" | 用於音訊書籍檔案。                                                                                                                                                               |
| "3A172A13-2BD9-4831-835B-114F6A95943F" | 適用于包含語音文字的音訊檔案，但不是音訊叢書。 例如，喜劇常式。                                                                           |
| "6677DB9B-E5A0-4063-A1AD-ACEB52840CF1" | 用於與新聞相關的音訊檔案。                                                                                                                                                    |
| "1B824A67-3F80-4E3E-9CDE-F7361B0F5F1B" | 用於具有交談顯示內容的音訊檔案。                                                                                                                                             |
| "1FE2E091-4E1E-40CE-B22D-348C732E0B10" | 用於與新聞相關的影片檔案。                                                                                                                                                    |
| "D6DE1D88-C77C-4593-BFBC-9C61E8C373E3" | 用於包含以網路為基礎的節目、短片、影片結尾等的影片檔案。 這是不適合另一個類別的影片娛樂一般識別碼。 |
| "00033368-5009-4AC3-A820-5D2D09A4E7C1" | 用於包含遊戲音訊剪輯的音訊檔案。                                                                                                                                  |
| "F24FF731-96FC-4D0F-A2F5-5A3483682B1A" | 用於包含遊戲音效軌完整歌曲的音訊檔案。 如果檔案中只編碼一部分的歌曲，請改用遊戲音訊剪輯的識別碼。                   |
| "E3E689E2-BA8C-4330-96DF-A0EEEFFA6876" | 用於包含音樂影片的影片檔案。                                                                                                                                            |
| "B76628F4-300D-443D-9CB5-01C285109DAF" | 用於包含一般家用影片的影片檔案。                                                                                                                                      |
| "A9B87FC9-BD47-4BF0-AC4F-655B89F7D868" | 用於包含功能短片的影片檔案。                                                                                                                                           |
| "BA7F258A-62F7-47A9-B21F-4651C42A000E" | 用於包含電視節目的影片檔案。 如果是以 Web 為基礎的節目，請使用更多的一般識別碼。                                                                                  |
| "44051B5B-B103-4B5C-92AB-93060A9463F0" | 用於包含公司影片的影片檔案。 例如，錄製的會議或訓練影片。                                                                                      |
| "0B710218-8C0C-475E-AF73-4C41C0C8F8CE" | 用於包含從相片製作之家用影片的影片檔案。                                                                                                                        |



 

指定次要類別識別碼時，檔案也應該包含主要類別識別碼屬性。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> <dt>

[**WM/MediaClassPrimaryID**](wm-mediaprimaryid.md)
</dt> </dl>

 

 




