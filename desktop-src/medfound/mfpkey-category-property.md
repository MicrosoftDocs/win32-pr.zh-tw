---
description: 包含媒體基礎轉換 (MFT) 的分類 GUID。
ms.assetid: 3c0948fc-42ea-4e43-a312-c98038020214
title: 'MFPKEY_CATEGORY 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbb83ab2c824ff9a4510e520b13c49ae5b3a52a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849520"
---
# <a name="mfpkey_category-property"></a>MFPKEY \_ CATEGORY 屬性

包含媒體基礎轉換 (MFT) 的分類 GUID。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

 (**CLSID** \*) 的 GUID

VT \_ CLSID

**puuid**



## <a name="remarks"></a>備註

這個屬性的值是可識別 MFT 類別目錄的 GUID。 如需分類清單，請參閱 [**MFT \_ 類別目錄**](mft-category.md)。

這個屬性是選擇性的，且僅供參考。 MFT 可以使用這個屬性來報告註冊它的類別。 若要取得此屬性，請查詢 **IPropertyStore** 介面的 MFT。

若要列舉 MFT 類別，請呼叫 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 函數。 **MFTEnum** 函式與這個屬性之間沒有直接連結。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[媒體基礎轉換](media-foundation-transforms.md)
</dt> </dl>

 

 




