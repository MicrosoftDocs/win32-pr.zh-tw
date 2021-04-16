---
title: 上傳限制
description: 若要限制上傳的大小，請設定 BITSMaximumUploadSize IIS 延伸模組屬性。
ms.assetid: 01ad2f32-18be-43a5-a07f-e6f28f7a471b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647aeefe82cf9c3ab035bc3e233c4157f471110b
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104462720"
---
# <a name="upload-limits"></a>上傳限制

若要限制上傳的大小，請設定 [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) IIS 延伸模組屬性。 在 IIS 7 中，您可能也必須修改 **maxAllowedContentLength** 屬性。 根據預設，IIS 7 上傳限制為30000000個位元組。 如需變更 IIS 預設值的詳細資訊和詳細資訊，請參閱 [KB942074](https://support.microsoft.com//kb/942074)。

 

 




