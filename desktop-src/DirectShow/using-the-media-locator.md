---
description: 使用媒體定位器
ms.assetid: 07840a37-7065-41e8-aee5-855c9f89fb77
title: 使用媒體定位器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce934b06d92c0bec66d9260a485516d3acaf5a9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945595"
---
# <a name="using-the-media-locator"></a>使用媒體定位器

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

媒體定位器是一個協助程式物件，可驗證檔案名，並在本機或網路目錄上搜尋遺失的檔案。 媒體偵測器會保留目錄路徑的快取，其中已在過去搜尋中成功找到檔案。 為了找出檔案，它會在其快取中搜尋目錄。 若失敗，媒體偵測器會顯示 [開啟檔案] 對話方塊，讓使用者以手動方式尋找檔案。 假設使用者找出檔案，則媒體定位器會將新的目錄新增至其快取。 媒體定位器會公開 [**IMediaLocator**](imedialocator.md) 介面。

一般來說，您的應用程式不會直接建立媒體定位器的實例。 相反地，時間軸和轉譯引擎會提供下列方法，以使用媒體偵測器來驗證檔案名。

-   若要在時間軸中驗證檔案名，請呼叫 [**IAMTimeline：： ValidateSourceNames**](iamtimeline-validatesourcenames.md)。 （選擇性）此方法也會使用正確的檔案名來更新來源物件。
-   若要在轉譯專案時驗證檔案名，請呼叫 [**IRenderEngine：： SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md)。

這兩種方法都採用旗標來控制媒體定位器的行為。 例如，您可以將搜尋限制為本機目錄。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用來源](working-with-sources.md)
</dt> </dl>

 

 



