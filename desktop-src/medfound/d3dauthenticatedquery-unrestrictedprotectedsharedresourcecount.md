---
description: 傳回任何進程可以開啟的受保護共用資源數目，而不受限制。
ms.assetid: afbd7bb9-de71-4992-919e-e1517228dc69
title: 'D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b2d834927d21c59ed5c70dcf3a001d100340405d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973195"
---
# <a name="d3dauthenticatedquery_unrestrictedprotectedsharedresourcecount"></a>D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT

傳回任何進程可以開啟的受保護共用資源數目，而不受限制。



| 需求 | 值 |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 查詢 GUID  | **D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**                                                                                                    |
| 輸入資料  | [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入**](d3dauthenticatedchannel-query-input.md)                                                                                   |
| 傳回資料 | [**D3DAUTHENTICATEDCHANNEL \_ QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT \_ 輸出**](d3dauthenticatedchannel-queryunrestrictedprotectedsharedresourcecount-output.md) |



 

## <a name="remarks"></a>備註

唯一支援此查詢的通道類型是 **D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 軟體**。

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

 

 




