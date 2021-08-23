---
description: 傳回與指定的 DirectX Video 加速 2 (DXVA-2) 解碼器裝置相關聯的密碼編譯會話和 Direct3D 裝置的控制碼。
ms.assetid: 90b3bcf3-2988-48de-8acd-62e385d4fdf0
title: 'D3DAUTHENTICATEDQUERY_CRYPTOSESSION (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 3ee1cabc69122ebd7eb7d81c64eb761439e6a3c0cde20dd376c3581b9aed0738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974667"
---
# <a name="d3dauthenticatedquery_cryptosession"></a>D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION

傳回與指定的 DirectX Video 加速 2 (DXVA-2) 解碼器裝置相關聯的密碼編譯會話和 Direct3D 裝置的控制碼。



| 需求 | 值 |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 查詢 GUID  | **D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**                                                                         |
| 輸入資料  | [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入**](d3dauthenticatedchannel-query-input.md)                             |
| 傳回資料 | [**D3DAUTHENTICATEDCHANNEL \_ QUERYCRYPTOSESSION \_ 輸出**](d3dauthenticatedchannel-querycryptosession-output.md) |



 

## <a name="remarks"></a>備註

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

 

 




