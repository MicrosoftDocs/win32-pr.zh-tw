---
title: 處理服務提供者中受保護的內容
description: 處理服務提供者中受保護的內容
ms.assetid: 5c18c8ec-d579-41df-8c25-c143fb9cdbef
keywords:
- Windows Media 裝置管理員，憑證
- 裝置管理員，憑證
- 程式設計指南，憑證
- 服務提供者，憑證
- 建立服務提供者，憑證
- certificates
- Windows Media 裝置管理員、受 DRM 保護的內容
- 裝置管理員，受 DRM 保護的內容
- 程式設計指南，受 DRM 保護的內容
- 服務提供者，受 DRM 保護的內容
- 建立服務提供者，受 DRM 保護的內容
- 受 DRM 保護的內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d10cf9078cf9aaf631b65de968f01491a97781
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106983285"
---
# <a name="handling-protected-content-in-the-service-provider"></a>處理服務提供者中受保護的內容

您可以建立服務提供者，以將受 DRM 保護的內容傳送至以可攜式裝置 DRM (PDDRM) 為基礎的裝置，但您無法建立服務提供者，以將受 DRM 保護的內容傳送至以 Windows Media DRM 10 為便攜裝置建立的裝置。 這些裝置會使用 MTP，您無法建立自己的 MTP 服務提供者。

服務提供者傳送 DRM 資料到 PDDRM 裝置必須採取的唯一額外步驟是取得 Microsoft 發出的憑證/金鑰組。 請參閱 [開發用的工具](tools-for-development.md) ，以瞭解要從何處取得此憑證/金鑰。 發給這些裝置的授權將會是簡化的授權，僅支援簡單播放的已購買內容;它們不會支援時間過期的授權。 Microsoft 針對 WMA/) WMV 檔案所提供的安全內容提供者 (會為您建立此授權，並將其儲存在傳送給服務提供者的檔標頭中。 您將不需要對受保護的檔案採取任何特殊步驟。

傳送受保護的檔案之後，Windows Media 裝置管理員會呼叫服務提供者，以向裝置要求特殊的授權儲存檔案。 Windows Media 裝置管理員會在此檔案中加入新授權的複本，並將其傳回給服務提供者，以傳送回裝置。 但是，即使服務提供者找不到或無法傳回此檔案，裝置仍應能使用檔案標頭中的授權複本來播放受保護的檔案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立服務提供者**](creating-a-service-provider.md)
</dt> <dt>

[**處理受保護的內容**](handling-protected-content.md)
</dt> </dl>

 

 




