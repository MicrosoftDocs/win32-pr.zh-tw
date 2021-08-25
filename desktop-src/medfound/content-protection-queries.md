---
description: 列出 IDirect3DAuthenticatedChannel9：： Query 方法的查詢。
ms.assetid: 75e246c6-bf23-44d9-8fb3-46a6dc5324a5
title: 內容保護查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c5aaa8c43cf722d13550ab4a1860e7a53780e7e82da7f374e28a7f599a22638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829088"
---
# <a name="content-protection-queries"></a>內容保護查詢

列出 [**IDirect3DAuthenticatedChannel9：： Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) 方法的查詢。



| 狀態要求                                                                                                                            | 描述                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md)                                   | 傳回用來將資料傳送至 GPU 的 i/o 匯流排類型。                                                                                                   |
| [**D3DAUTHENTICATEDQUERY \_ CHANNELTYPE**](d3dauthenticatedquery-channeltype.md)                                                           | 傳回已驗證通道的類型。                                                                                                                  |
| [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md)                                                       | 傳回與指定的 DirectX Video 加速 2 (DXVA-2) 解碼器裝置相關聯的密碼編譯會話和 Direct3D 裝置的控制碼。 |
| [**D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedquery-currentencryptionwhenaccessible.md)                   | 傳回在 CPU 或匯流排可以存取內容之前套用的加密類型。                                                            |
| [**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md)                                                         | 傳回與這個已驗證通道相關聯之裝置的控制碼。                                                                          |
| [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md)                         | 傳回可供 CPU 或匯流排存取之前，用來加密內容的其中一種加密類型。                                     |
| [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md)               | 傳回可供 CPU 或匯流排存取之前，用來加密內容的加密類型數目。                                  |
| [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md)                                                                 | 傳回與指定的密碼編譯會話和 Direct3D 裝置相關聯的其中一個輸出識別碼。                                        |
| [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md)                                                       | 傳回與指定的密碼編譯會話和 Direct3D 裝置相關聯的輸出識別碼數目。                                             |
| [**D3DAUTHENTICATEDQUERY \_ 保護**](d3dauthenticatedquery-protection.md)                                                             | 傳回裝置目前的保護層級。                                                                                                        |
| [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md)                   | 傳回允許以限制存取開啟共用資源之進程的相關資訊。                                                        |
| [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md)         | 傳回允許以限制存取開啟共用資源的進程數目。                                                           |
| [**D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) | 傳回任何進程可以開啟且沒有限制的受保護共用資源數目。                                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 影片 Api](direct3d-video-apis.md)
</dt> <dt>

[以 GPU 為基礎的內容保護](gpu-based-content-protection.md)
</dt> </dl>

 

 



