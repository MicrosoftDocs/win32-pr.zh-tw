---
title: DRM 網路作業
description: DRM 網路作業
ms.assetid: 4a10c811-2aa1-4b97-8a72-61e8b04075a8
keywords:
- Windows Media Format SDK，DRM 網路作業
- Advanced Systems Format (ASF) 、DRM 網路作業
- ASF (Advanced Systems Format) ，DRM 網路作業
- 數位版權管理 (DRM) ，網路作業
- DRM (數位版權管理) ，網路作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 875186e43e066d71847da014468e9b1764b60cf2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300224"
---
# <a name="drm-network-operations"></a>DRM 網路作業

數個 DRM 相關的作業需要您的應用程式連接到在網路上執行的服務。 這些作業包括了個人化、授權取得、授權撤銷，以及授權備份和還原。

就像任何網路交易一樣，當您的應用程式包含需要網路作業的功能時，您的應用程式應該要考慮各種難題。 您的應用程式應該將作業的狀態追蹤至特定功能的任何可能範圍，通常是藉由處理狀態訊息。 您應該將意見反應提供給使用者的狀態。 如果第一次嘗試時作業失敗，您應該讓使用者有機會重試。 在許多情況下，第一次嘗試會遇到困難，但後續的嘗試會完成，而不會發生錯誤。

> [!Note]  
> 此 SDK 的 x64 版本不支援 DRM。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**啟用 DRM 支援**](enabling-drm-support.md)
</dt> </dl>

 

 




