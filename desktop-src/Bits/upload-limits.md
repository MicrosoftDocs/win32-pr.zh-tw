---
title: Upload限制
description: 若要限制上傳的大小，請設定 BITSMaximumUploadSize IIS 延伸模組屬性。
ms.assetid: 01ad2f32-18be-43a5-a07f-e6f28f7a471b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee151535fa9a8d782de2dcadf2dce63c8e29c941c6adacfa27e351cfafa5c512
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588528"
---
# <a name="upload-limits"></a>Upload限制

若要限制上傳的大小，請設定 [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) IIS 延伸模組屬性。 在 IIS 7 中，您可能也必須修改 **maxAllowedContentLength** 屬性。 根據預設，IIS 7 上傳限制為30000000個位元組。 如需變更 IIS 預設值的詳細資訊和詳細資訊，請參閱 [KB942074](https://support.microsoft.com//kb/942074)。

 

 




