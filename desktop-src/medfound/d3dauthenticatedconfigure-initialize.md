---
description: 初始化已驗證的通道。
ms.assetid: a74edbaa-af57-4f8e-9974-f6053f59377f
title: 'D3DAUTHENTICATEDCONFIGURE_INITIALIZE (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_INITIALIZE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2cd3238b7a7eea27356ce76ec9c83bf8aea4d7f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971153"
---
# <a name="d3dauthenticatedconfigure_initialize"></a>D3DAUTHENTICATEDCONFIGURE \_ INITIALIZE

初始化已驗證的通道。



| 需求 | 值 |
|--------------|-----------------------------------------------------------------------------------------------------|
| 命令 GUID | **D3DAUTHENTICATEDCONFIGURE \_ INITIALIZE**                                                           |
| 輸入資料   | [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREINITIALIZE**](d3dauthenticatedchannel-configureinitialize.md) |



 

## <a name="remarks"></a>備註

在會話開始時傳送此命令一次。 每個已驗證的通道只能傳送一次此命令。 此命令會忽略輸入的序號。

下列通道類型支援此命令：

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

[內容保護命令](content-protection-commands.md)
</dt> <dt>

[以 GPU 為基礎的內容保護](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




