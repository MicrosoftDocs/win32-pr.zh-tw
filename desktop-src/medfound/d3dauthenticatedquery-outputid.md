---
description: 傳回與指定的密碼編譯會話和 Direct3D 裝置相關聯的其中一個輸出識別碼。
ms.assetid: 7b56055a-fb36-4e54-9bee-ab9401b09267
title: 'D3DAUTHENTICATEDQUERY_OUTPUTID (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: fa970ae6e7b10f553679376d7a924d1c8b67c595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689324"
---
# <a name="d3dauthenticatedquery_outputid"></a>D3DAUTHENTICATEDQUERY \_ OUTPUTID

傳回與指定的密碼編譯會話和 Direct3D 裝置相關聯的其中一個輸出識別碼。



| 需求 | 值 |
|-------------|--------------------------------------------------------------------------------------------------------|
| 查詢 GUID  | **D3DAUTHENTICATEDQUERY \_ OUTPUTID**                                                                    |
| 輸入資料  | [**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTID \_ 輸入**](d3dauthenticatedchannel-queryoutputid-input.md)   |
| 傳回資料 | [**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTID \_ 輸出**](d3dauthenticatedchannel-queryoutputid-output.md) |



 

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

 

 




