---
description: 傳回與指定的密碼編譯會話和 Direct3D 裝置相關聯的輸出識別碼數目。
ms.assetid: a5b17250-6a40-40a9-93b6-3b98b56b09d6
title: 'D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: c6a3da90d467701decfe5f96383e06026325e86c2622ec0f05f4703b06e2cbe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828508"
---
# <a name="d3dauthenticatedquery_outputidcount"></a>D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT

傳回與指定的密碼編譯會話和 Direct3D 裝置相關聯的輸出識別碼數目。



| 需求 | 值 |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 查詢 GUID  | **D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**                                                                         |
| 輸入資料  | [**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_ 輸入**](d3dauthenticatedchannel-queryoutputidcount-input.md)   |
| 傳回資料 | [**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_ 輸出**](d3dauthenticatedchannel-queryoutputidcount-output.md) |



 

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

 

 




