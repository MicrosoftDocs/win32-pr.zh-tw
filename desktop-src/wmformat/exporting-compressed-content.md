---
title: 匯出壓縮的內容
description: 匯出壓縮的內容
ms.assetid: b312aa5e-d693-4d0a-9d74-b443713cec8c
keywords:
- Windows媒體格式 SDK，DRM 匯出
- Windows媒體格式 SDK，匯出
- Windows媒體格式 SDK，壓縮的內容
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
ms.openlocfilehash: 20e7e8e6d71e4104d65336b131d0e15d5eaedd8b2fba4b7715f5e60aa6083544
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055498"
---
# <a name="exporting-compressed-content"></a>匯出壓縮的內容

本節說明如何在應用程式接收壓縮數位媒體資料的 Windows 媒體檔案上，匯出 Windows 媒體 DRM 保護的媒體。 若要這樣做，您的應用程式必須在 ASF 檔案中執行所有 Windows 媒體 DRM 加密承載的內嵌解密。

> [!Note]  
> 系統會提供 ASF 剖析程式庫，作為 Windows 媒體 DRM 匯出合約的一部分。

 

匯出壓縮內容所涉及的主要步驟如下：

1.  視需要執行 DRM 的個人化。
2.  確認已明確允許目標內容保護設定。
3.  建立解密器物件來解密每個 ASF 承載。
4.  DRM 系統會將 Windows 媒體 DRM 的每個 ASF 承載 transcrypts 至 RC4，然後再將它傳遞至您的應用程式。

如果您的應用程式在 transcryption 期間變更了 ASF 承載的大小，您也必須 remultiplex ASF 檔案。

將 Windows 媒體 DRM 匯出應用程式憑證傳遞給存根程式庫。 憑證經過驗證，如果有效，DRM 系統會產生初始化向量，並使用 RSA OAEP 進行加密。

-   藉由串連初始化向量和 salt 值，為每個承載建立 RC4 工作階段金鑰。 您將 salt 值提供給解密 API，您必須為每個承載將它遞增為非零的正整數值。

您將會在 Windows 媒體 DRM 匯出合約中提供一項工具，讓您能夠產生自己的 RSA 公開/私密金鑰組。 您會將公開金鑰傳送給 microsoft，microsoft 會將它併入簽署的 Windows 媒體 DRM 應用程式憑證，並將其傳回。

每個裝載在使用 RC4 解密金鑰進行解密之後，都必須立即加密至輸出 CPS。 處理未加密的承載有其他限制，也就是 Windows 媒體 DRM 匯出合約隨附的健全狀況與合規性規則中所述。

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

 

 




