---
description: 將密碼編譯會話與 DirectX Video 加速 2 (DXVA-2) 解碼器裝置和 Direct3D 裝置產生關聯。
ms.assetid: d40fead7-8a86-426e-933e-13df21cdf50b
title: 'D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 3e1df4b58750d5b2d82eb518d5dfc0ef24bdbe4e5569ebcaf708b8df60691d04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449438"
---
# <a name="d3dauthenticatedconfigure_cryptosession"></a>D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION

將密碼編譯會話與 DirectX Video 加速 2 (DXVA-2) 解碼器裝置和 Direct3D 裝置產生關聯。



| 需求 | 值 |
|--------------|-----------------------------------------------------------------------------------------------------------|
| 命令 GUID | **D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION**                                                              |
| 輸入資料   | [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURECRYPTOSESSION**](d3dauthenticatedchannel-configurecryptosession.md) |



 

## <a name="remarks"></a>備註

傳送這個命令之後，您可以傳送 [D3DAUTHENTICATEDQUERY \_ OUTPUTID](d3dauthenticatedquery-outputid.md) 查詢，找出哪些影片輸出與密碼編譯會話相關聯。

下列通道類型支援此命令：

-   **D3DAUTHENTICATEDCHANNEL \_ D3D9**
-   **D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 軟體**

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[內容保護命令](content-protection-commands.md)
</dt> <dt>

[以 GPU 為基礎的內容保護](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




