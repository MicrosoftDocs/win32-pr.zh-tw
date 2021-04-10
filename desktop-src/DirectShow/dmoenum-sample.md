---
description: DMOEnum 範例
ms.assetid: afd7853e-b0ab-42f6-8c2e-c2b0b40d989b
title: DMOEnum 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c413b7787ba12785758cffed89be15229373643d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187550"
---
# <a name="dmoenum-sample"></a>DMOEnum 範例

## <a name="description"></a>Description

這個範例應用程式會列舉所有的 [DirectX 媒體物件](directx-media-objects.md) (DMOs) 在使用者的系統中註冊，並顯示其相關資訊。

此範例會使用 [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) 函數和 [**IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) 介面來列舉 DMOs。 它會使用 [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) 介面和其他的 sql-dmo 介面，來取得每個的資訊。

## <a name="usage"></a>使用方式

當應用程式啟動時，它會列舉所有已安裝的 DMOs。 如果您選取特定的 SQL-DMO 類別，應用程式只會顯示該類別中的 DMOs。 若要查看一組的相關資訊，請從清單中選取 []。 應用程式會顯示資料流程的數目、慣用的媒體類型、該的 DLL 伺服器，以及該的其他資訊。 若要包含或排除索引 DMOs，請切換 [ **包含金鑰 DMOs？** ] 核取方塊。

## <a name="downloading-the-sample"></a>下載範例

若要下載 DirectShow SDK 範例，請安裝最新版本的 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。

此範例安裝在下列路徑下： *\[ SDK \] 根* \\ 範例 \\ 多媒體 \\ DirectShow \\ 其他 \\ DMOEnum。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 範例](directshow-samples.md)
</dt> </dl>

 

 



