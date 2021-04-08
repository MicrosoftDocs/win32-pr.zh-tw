---
title: WM/圖片
description: WM/圖片屬性包含與內容相關的圖片。
ms.assetid: ec82dfdf-7755-4758-9771-096aac114f78
keywords:
- WM/Picture windows 媒體格式
topic_type:
- apiref
api_name:
- WM/Picture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ba3f74378112c8e3f58958db8b22c970e8e099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103932692"
---
# <a name="wmpicture"></a>WM/圖片

**WM/圖片** 屬性包含與內容相關的圖片。

## <a name="global-constant"></a>全域常數

g \_ wszWMPicture

## <a name="data-type"></a>資料類型

[**WM \_圖片**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**WMT \_ 類型 \_ BINARY**) 

## <a name="remarks"></a>備註

這個屬性與 ID3 框架（APIC）相容。 APIC 框架的 ID3 規格規定，雖然可能有任意數目的 APIC 框架與檔案相關聯，但只有一個類型可以是1，而且只有一個類型是2。 規格也會指出圖片描述的長度不能超過64個字元，但可以是空的。

使用 Windows Media 格式 SDK 的物件新增的 WM/圖片屬性不會自動進行驗證，以符合 ID3 規格。 如果您想要維持與 ID3 的完整相容性，您必須在應用程式中加入程式碼以執行驗證。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> <dt>

[**WM \_ 圖片**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)
</dt> </dl>

 

 




