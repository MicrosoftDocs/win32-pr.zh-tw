---
description: 傳回裝置目前的保護層級。
ms.assetid: 335d21e8-2a98-4824-a60d-1969a40e8d24
title: 'D3DAUTHENTICATEDQUERY_PROTECTION (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_PROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2cd91ee37187d8b2a6906d88832d06250b05c572d789d15db3b5621f78b890ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742608"
---
# <a name="d3dauthenticatedquery_protection"></a>D3DAUTHENTICATEDQUERY \_ 保護

傳回裝置目前的保護層級。



| 需求 | 值 |
|-------------|------------------------------------------------------------------------------------------------------------|
| 查詢 GUID  | **D3DAUTHENTICATEDQUERY \_ 保護**                                                                      |
| 輸入資料  | [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入**](d3dauthenticatedchannel-query-input.md)                       |
| 傳回資料 | [**D3DAUTHENTICATEDCHANNEL \_ QUERYPROTECTION \_ 輸出**](d3dauthenticatedchannel-queryprotection-output.md) |



 

## <a name="remarks"></a>備註

此查詢對於所有通道類型都有效。

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

 

 




