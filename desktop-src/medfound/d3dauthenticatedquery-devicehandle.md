---
description: 傳回與這個已驗證通道相關聯之裝置的控制碼。
ms.assetid: 948eac1a-640a-47fd-b538-1de3ea5d8f0b
title: 'D3DAUTHENTICATEDQUERY_DEVICEHANDLE (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_DEVICEHANDLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a3ebf54530a4ae029a52632eb5bb5afc51b5f152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973795"
---
# <a name="d3dauthenticatedquery_devicehandle"></a>D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE

傳回與這個已驗證通道相關聯之裝置的控制碼。 您可以使用此控制碼來確認兩個已驗證的通道是否與相同裝置通訊。



| 需求 | 值 |
|-------------|----------------------------------------------------------------------------------------------------------------|
| 查詢 GUID  | **D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**                                                                        |
| 輸入資料  | [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入**](d3dauthenticatedchannel-query-input.md)                           |
| 傳回資料 | [**D3DAUTHENTICATEDCHANNEL \_ QUERYDEVICEHANDLE \_ 輸出**](d3dauthenticatedchannel-querydevicehandle-output.md) |



 

## <a name="remarks"></a>備註

此查詢對於所有通道類型都有效。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[內容保護查詢](content-protection-queries.md)
</dt> <dt>

[以 GPU 為基礎的內容保護](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9：： Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




