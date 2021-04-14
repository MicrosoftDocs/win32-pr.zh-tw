---
title: WM/曲目
description: WM/Track 屬性包含內容的曲目編號。 這個屬性是以零為基底，而且支援回溯相容性。 新內容應該改用 WM/TrackNumber 屬性。
ms.assetid: c763d7b0-9d12-4a4e-8c9f-9cf67bd2a02b
keywords:
- WM/Track windows 媒體格式
topic_type:
- apiref
api_name:
- WM/Track
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 244426175ea74bc0281f8822964c2fc0bfa37aa7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104372781"
---
# <a name="wmtrack"></a>WM/曲目

**WM/Track** 屬性包含內容的曲目編號。 這個屬性是以零為基底，而且支援回溯相容性。 新內容應該改用 [**WM/TrackNumber**](wm-tracknumber.md) 屬性。

## <a name="global-constant"></a>全域常數

g \_ wszWMTrack

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ 字串**

## <a name="remarks"></a>備註

許多現有的應用程式都會將 **WM/Track** 的值寫入為 **DWORD**。 如果您建立的應用程式會播放來自不明來源的檔案，您應該包含程式碼來處理字串和 **DWORD** 值。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




