---
description: 傳回用來將資料傳送至 GPU 的 i/o 匯流排類型。
ms.assetid: 5a180a5c-6798-40ba-9e2c-ce1f755fcc08
title: 'D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9d7d4daaec3d52b7aabafe61c5763304c400b6a36be1367e01b0a9163f2f9e38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828678"
---
# <a name="d3dauthenticatedquery_accessibilityattributes"></a>D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES

傳回用來將資料傳送至 GPU 的 i/o 匯流排類型。



| 需求 | 值 |
|-------------|--------------------------------------------------------------------------------------------------------------|
| 查詢 GUID  | **D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**                                                           |
| 輸入資料  | [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入**](d3dauthenticatedchannel-query-input.md)                         |
| 傳回資料 | [**D3DAUTHENTICATEDCHANNEL \_ QUERYINFOBUSTYPE \_ 輸出**](d3dauthenticatedchannel-queryinfobustype-output.md) |



 

## <a name="remarks"></a>備註

此查詢也會傳回將內容放入視訊記憶體時可存取的相關資訊。

下列通道類型支援此查詢：

-   **D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 硬體**
-   **D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 軟體**

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[內容保護查詢](content-protection-queries.md)
</dt> <dt>

[以 GPU 為基礎的內容保護](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9：： Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




