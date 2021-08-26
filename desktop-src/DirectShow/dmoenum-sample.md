---
description: DMOEnum 範例
ms.assetid: afd7853e-b0ab-42f6-8c2e-c2b0b40d989b
title: DMOEnum 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6fc51cc45ad879ccbc5ccd232b782e4b9f5511071d8d2492c135efcb322969c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079198"
---
# <a name="dmoenum-sample"></a>DMOEnum 範例

## <a name="description"></a>描述

這個範例應用程式會列舉所有的 [DirectX 媒體物件](directx-media-objects.md) (DMOs) 在使用者的系統中註冊，並顯示其相關資訊。

此範例會使用 [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) 函數和 [**IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) 介面來列舉 DMOs。 它會使用 [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject)介面和其他 DMO 介面，來取得每個 DMO 的相關資訊。

## <a name="usage"></a>使用方式

當應用程式啟動時，它會列舉所有已安裝的 DMOs。 如果您選取特定的 DMO 類別目錄，應用程式只會顯示該類別中的 DMOs。 若要查看 DMO 的相關資訊，請從清單中選取 DMO。 應用程式會顯示資料流程的數目、慣用的媒體類型、該 DMO 的 DLL 伺服器，以及 DMO 的其他相關資訊。 若要包含或排除索引 DMOs，請切換 [ **包含金鑰 DMOs？** ] 核取方塊。

## <a name="downloading-the-sample"></a>下載範例

若要下載 DirectShow SDK 範例，請安裝最新版本的[Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。

此範例安裝在下列路徑下： *\[ SDK \] 根* \\ 範例 \\ 多媒體 \\ DirectShow \\ 其他 \\ DMOEnum。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow樣品](directshow-samples.md)
</dt> </dl>

 

 



