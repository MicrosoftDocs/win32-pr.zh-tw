---
title: 匯出壓縮的內容
description: 匯出壓縮的內容
ms.assetid: b312aa5e-d693-4d0a-9d74-b443713cec8c
keywords:
- Windows Media Format SDK，DRM 匯出
- Windows Media 格式 SDK，匯出
- Windows Media Format SDK，壓縮的內容
- 數位版權管理 (DRM) 、匯出
- DRM (數位版權管理) ，匯出
- 數位版權管理 (DRM) ，壓縮的內容
- DRM (數位版權管理) ，壓縮的內容
- DRM 用戶端擴充 Api，壓縮的內容
- 用戶端擴充的 Api，壓縮的內容
- DRM 用戶端擴充 Api，匯出
- 用戶端擴充 Api，匯出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37781d5575dbffb7103f07307a149f4bd5e9e4fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839803"
---
# <a name="exporting-compressed-content"></a>匯出壓縮的內容

本節說明如何在應用程式接收壓縮數位媒體資料的 Windows Media 檔案上，匯出 Windows Media 受 DRM 保護的媒體。 若要這樣做，您的應用程式必須在 ASF 檔案中執行所有 Windows Media DRM 加密承載的內嵌解密。

> [!Note]  
> 系統會提供 ASF 剖析程式庫，作為 Windows Media DRM 匯出合約的一部分。

 

匯出壓縮內容所涉及的主要步驟如下：

1.  視需要執行 DRM 的個人化。
2.  確認已明確允許目標內容保護設定。
3.  建立解密器物件來解密每個 ASF 承載。
4.  DRM 系統會先將 Windows Media DRM 的每個 ASF 承載 transcrypts 至 RC4，再將其傳遞至您的應用程式。

如果您的應用程式在 transcryption 期間變更了 ASF 承載的大小，您也必須 remultiplex ASF 檔案。

傳遞給存根程式庫 Windows Media DRM 匯出應用程式憑證。 憑證經過驗證，如果有效，DRM 系統會產生初始化向量，並使用 RSA OAEP 進行加密。

-   藉由串連初始化向量和 salt 值，為每個承載建立 RC4 工作階段金鑰。 您將 salt 值提供給解密 API，您必須為每個承載將它遞增為非零的正整數值。

您將在 Windows Media DRM 匯出合約中提供 Microsoft 所提供的工具，可讓您產生自己的 RSA 公開/私密金鑰組。 您會將公開金鑰傳送給 Microsoft，Microsoft 會將它併入已簽署的 Windows Media DRM 應用程式憑證，並將其傳回。

每個裝載在使用 RC4 解密金鑰進行解密之後，都必須立即加密至輸出 CPS。 在 Windows Media DRM 匯出合約隨附的健全狀況與合規性規則中，處理未加密的承載有其他限制。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ASF 承載解密和重新加密**](asf-payload-decryption-and-re-encryption.md)
</dt> <dt>

[**DRM 匯出**](drm-export.md)
</dt> <dt>

[**執行 DRM 的個人化**](performing-drm-individualization.md)
</dt> <dt>

[**驗證與初始化**](verification-and-initialization.md)
</dt> </dl>

 

 




