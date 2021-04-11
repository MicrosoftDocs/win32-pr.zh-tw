---
description: 傳回在 CPU 或匯流排可以存取內容之前套用的加密類型。
ms.assetid: 89526bb2-1316-4730-b599-3690b1838c3e
title: 'D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a8b3374e6d50a50d32b60113318e5d1099083226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191065"
---
# <a name="d3dauthenticatedquery_currentencryptionwhenaccessible"></a>D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE

傳回在 CPU 或匯流排可以存取內容之前套用的加密類型。



| 需求 | 值 |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 查詢 GUID  | **D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**                                                                                   |
| 輸入資料  | [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入**](d3dauthenticatedchannel-query-input.md)                                                         |
| 傳回資料 | [**D3DAUTHENTICATEDCHANNEL \_ QUERYUNCOMPRESSEDENCRYPTIONLEVEL \_ 輸出**](d3dauthenticatedchannel-queryuncompressedencryptionlevel-output.md) |



 

## <a name="remarks"></a>備註

下列通道類型支援此查詢：

-   **D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 硬體**
-   **D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 軟體**

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

 

 




