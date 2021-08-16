---
description: Windows可攜式裝置支援下列影片內容。
ms.assetid: e6df5b2d-ceb8-4de0-b60b-9102c77143fe
title: '影片屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Video
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 6e7bbab3416f50a95d2ae29e2be0ef5ecdcad6eed0112f940e5c34b593f2b79a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083382"
---
# <a name="video-properties"></a>影片屬性

Windows可攜式裝置支援下列影片內容。



| 屬性                                         | VarType        | 描述                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 影片 \_ 作者**                           | **VT \_ LPWSTR** | 影片檔案的作者。                                                                                                                                                                                                                           |
| **WPD \_ 影片 \_ 位元速率**                          | **VT \_ UI4**    | 影片檔案的位元速率。                                                                                                                                                                                                                         |
| **WPD \_ 影片 \_ 緩衝區 \_ 大小**                     | **VT \_ UI4**    | 值，指定轉譯此檔案所需的影片緩衝區大小。                                                                                                                                                                              |
| **WPD \_ 影片 \_ 點數**                          | **VT \_ LPWSTR** | 列出影片轉換和小組的信用額度。                                                                                                                                                                                                    |
| **WPD \_ VIDEO \_ FOURCC 程式 \_ 代碼**                     | **VT \_ DWORD**  | 註冊的 FourCC 程式碼，指出用於影片檔案的編解碼器。 如需 FourCC 格式的清單，請參閱 MSDN 網站上的 [註冊的 FourCC 碼和 WAVE 格式](https://msdn2.microsoft.com/library/ms867195.aspx) 文章。 |
| **WPD \_ 影片的 \_ 畫面播放速率**                        | **VT \_ UI4**    | 影片檔案的畫面播放速率，以框架/秒 x 1000 為限。 例如，畫面播放速率29.97 表示為29970。                                                                                                                                 |
| **WPD \_ 影片內容類型 \_**                            | **VT \_ LPWSTR** | 此影片檔案的類型。 沒有標準的內容類型定義。                                                                                                                                                                                  |
| **WPD \_ 影片 \_ 主要 \_ 畫面 \_ 距離**             | **VT \_ UI4**    | 主要畫面格之間的間隔（以毫秒為單位）。                                                                                                                                                                                                       |
| **WPD \_ 視頻 \_ 品質 \_ 設定**                 | **VT \_ UI4**    | 影片檔案的品質設定。 這與編解碼器相依。                                                                                                                                                                                        |
| **WPD \_ VIDEO \_ RECORDEDTV \_ CHANNEL \_ NUMBER**      | **VT \_ UI4**    | 錄製影片的電視頻道號碼。                                                                                                                                                                                              |
| **WPD \_ VIDEO \_ RECORDEDTV \_ 節目 \_ 說明** | **VT \_ LPWSTR** | 錄製的電視節目描述。                                                                                                                                                                                                       |
| **WPD \_ VIDEO \_ RECORDEDTV \_ REPEAT**               | **VT \_ BOOL**   | 指定電視節目是否重複顯示的布林值。                                                                                                                                                                     |
| **WPD \_ VIDEO \_ RECORDEDTV \_ 站 \_ 名稱**        | **VT \_ LPWSTR** | 影片錄製來源的電視電臺。                                                                                                                                                                                                |
| **WPD \_ 影片 \_ 掃描 \_ 類型**                       | **VT \_ UI4**    | [**WPD \_ 影片 \_ 掃描 \_ 類型**](wpd-video-scan-types.md)列舉值，指定影片檔案的交錯。                                                                                                                                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WPD 屬性和屬性**](properties-and-attributes.md)
</dt> </dl>

 

 




