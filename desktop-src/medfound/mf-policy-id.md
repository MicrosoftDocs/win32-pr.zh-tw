---
description: 可以在 IMFOutputPolicy 上設定的識別碼。
ms.assetid: 89da33c8-97af-4c56-8bdb-2ac588810d77
title: MF_POLICY_ID (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1702f990dc1c88f7632bf74a40ca4671a70350450c723d4d9392af6e47dac038
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740664"
---
# <a name="mf_policy_id-attribute"></a>MF \_ 原則 \_ 識別碼屬性

可以在 [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy)上設定的識別碼。

## <a name="data-type"></a>資料類型

**UINT32** (視為 **BOOL**) 

## <a name="remarks"></a>備註

您可以從 [MEPolicySet](./mepolicyset.md) 媒體事件接收值。 它會儲存為 **MEPolicySet** 事件中的 **VT_UI4** 型別承載。


## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 102020年4月更新   <br/>                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>



 

 
