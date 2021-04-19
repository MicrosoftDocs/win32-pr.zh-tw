---
description: 描述 Microsoft Direct3D 9 video 介面所使用的結構。
ms.assetid: 584c087e-53f0-42d8-99ed-a0d013379363
title: Direct3D 9 影片結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ac8e03ff524f7f943c6adbee39b57785112a3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986277"
---
# <a name="direct3d-9-video-structures"></a>Direct3D 9 影片結構

描述 Microsoft Direct3D 9 video 介面所使用的結構。



| 結構                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D \_ OMAC**](d3d-omac.md)<br/> 包含訊息驗證碼 (MAC) 。<br/>                                                                                                                                                                                                                                                                        |
| [**D3DAES \_ CTR \_ IV**](d3daes-ctr-iv.md)<br/> 包含 (IV) 的初始化向量。<br/>                                                                                                                                                                                                                                                                   |
| [**D3DAUTHENTICATEDCHANNEL \_ 設定 \_ 輸入**](d3dauthenticatedchannel-configure-input.md)<br/> 包含 [**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) 方法的輸入資料。<br/>                                                                                                                     |
| [**D3DAUTHENTICATEDCHANNEL \_ 設定 \_ 輸出**](d3dauthenticatedchannel-configure-output.md)<br/> 包含對 [**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) 方法之呼叫的回應。<br/>                                                                                                        |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREINITIALIZE**](d3dauthenticatedchannel-configureinitialize.md)<br/> 包含 [**D3DAUTHENTICATEDCONFIGURE \_ INITIALIZE**](d3dauthenticatedconfigure-initialize.md) 命令的輸入資料。<br/>                                                                                                                       |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREPROTECTION**](d3dauthenticatedchannel-configureprotection.md)<br/> 包含 [**D3DAUTHENTICATEDCONFIGURE \_ 保護**](d3dauthenticatedconfigure-protection.md) 命令的輸入資料。<br/>                                                                                                                       |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURECRYPTOSESSION**](d3dauthenticatedchannel-configurecryptosession.md)<br/> 包含 [**D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) 命令的輸入資料。<br/>                                                                                                           |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURESHAREDRESOURCE**](d3dauthenticatedchannel-configuresharedresource.md)<br/> 包含 [**D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE**](d3dauthenticatedconfigure-sharedresource.md) 命令的輸入資料。<br/>                                                                                                       |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREUNCOMPRESSEDENCRYPTION**](d3dauthenticatedchannel-configureuncompressedencryption.md)<br/> 包含 [**D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) 命令的輸入資料。<br/>                                                                   |
| [**D3DAUTHENTICATEDCHANNEL \_ 保護 \_ 旗標**](d3dauthenticatedchannel-protection-flags.md)<br/> 指定影片內容的保護層級。<br/>                                                                                                                                                                                                   |
| [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入**](d3dauthenticatedchannel-query-input.md)<br/> 包含 [**IDirect3DAuthenticatedChannel9：： Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) 方法的輸入資料。<br/>                                                                                                                                     |
| [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸出**](d3dauthenticatedchannel-query-output.md)<br/> 包含對 [**IDirect3DAuthenticatedChannel9：： Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) 方法之呼叫的回應。<br/>                                                                                                                        |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYCHANNELTYPE \_ 輸出**](d3dauthenticatedchannel-querychanneltype-output.md)<br/> 包含對 [**D3DAUTHENTICATEDQUERY \_ CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) 查詢的回應。<br/>                                                                                                                     |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYCRYPTOSESSION \_ 輸入**](d3dauthenticatedchannel-querycryptosession-input.md)<br/> 包含 [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) 查詢的輸入資料。<br/>                                                                                                                |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYCRYPTOSESSION \_ 輸出**](d3dauthenticatedchannel-querycryptosession-output.md)<br/> 包含對 [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) 查詢的回應。<br/>                                                                                                             |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYDEVICEHANDLE \_ 輸出**](d3dauthenticatedchannel-querydevicehandle-output.md)<br/> 包含對 [**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) 查詢的回應。<br/>                                                                                                                 |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUID \_ 輸入**](d3dauthenticatedchannel-queryevictionencryptionguid-input.md)<br/> 包含 [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) 查詢的輸入資料。<br/>                                                                |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUID \_ 輸出**](d3dauthenticatedchannel-queryevictionencryptionguid-output.md)<br/> 包含對 [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) 查詢的回應。<br/>                                                             |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUIDCOUNT \_ 輸出**](d3dauthenticatedchannel-queryevictionencryptionguidcount-output.md)<br/> 包含對 [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md) 查詢的回應。<br/>                                         |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYINFOBUSTYPE \_ 輸出**](d3dauthenticatedchannel-queryinfobustype-output.md)<br/> 包含對 [**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md) 查詢的回應。<br/>                                                                                             |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTID \_ 輸入**](d3dauthenticatedchannel-queryoutputid-input.md)<br/> 包含 [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md) 查詢的 intput 資料。<br/>                                                                                                                                   |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTID \_ 輸出**](d3dauthenticatedchannel-queryoutputid-output.md)<br/> 包含對 [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md) 查詢的回應。<br/>                                                                                                                                 |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_ 輸入**](d3dauthenticatedchannel-queryoutputidcount-input.md)<br/> 包含 [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) 查詢的輸入資料。<br/>                                                                                                                |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_ 輸出**](d3dauthenticatedchannel-queryoutputidcount-output.md)<br/> 包含對 [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) 查詢的回應。<br/>                                                                                                             |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYPROTECTION \_ 輸出**](d3dauthenticatedchannel-queryprotection-output.md)<br/> 包含對 [**D3DAUTHENTICATEDQUERY \_ PROTECTION**](d3dauthenticatedquery-protection.md) 查詢的回應。<br/>                                                                                                                         |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ 輸入**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-input.md)<br/> 包含 [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) 查詢的輸入資料。<br/>                                        |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ 輸出**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md)<br/> 包含對 [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) 查詢的回應。<br/>                                     |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT \_ 輸出**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocesscount-output.md)<br/> 包含對 [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) 查詢的回應。<br/>                 |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYUNCOMPRESSEDENCRYPTIONLEVEL \_ 輸出**](d3dauthenticatedchannel-queryuncompressedencryptionlevel-output.md)<br/> 包含對 [**D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedquery-currentencryptionwhenaccessible.md) 查詢的回應。<br/>                                             |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT \_ 輸出**](d3dauthenticatedchannel-queryunrestrictedprotectedsharedresourcecount-output.md)<br/> 包含對 [**D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) 查詢的回應。<br/> |
| [**D3DCONTENTPROTECTIONCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps)<br/> 描述顯示驅動程式的內容保護功能。<br/>                                                                                                                                                                                                                    |
| [**D3DENCRYPTED \_ 區塊 \_ 資訊**](d3dencrypted-block-info.md)<br/> 指定要在受保護的視頻界面中加密的位元組。<br/>                                                                                                                                                                                                                     |
| [**D3DOVERLAYCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3doverlaycaps)<br/> 指定 Direct3D 裝置的硬體重迭功能。<br/>                                                                                                                                                                                                                                            |
| [**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo)<br/> 指定 [**IDirect3DDXVADevice9：： Execute**](idirect3ddxvadevice9-execute.md) 方法的緩衝區。<br/>                                                                                                                                                                                                  |
| [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo)<br/> 指定 DirectX Video 加速 (DXVA) 的壓縮表面需求。<br/>                                                                                                                                                                                                         |
| [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo)<br/> 指定 DXVA 影片解碼之未壓縮表面的維度和像素格式。<br/>                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 影片 Api](direct3d-video-apis.md)
</dt> </dl>

 

 




