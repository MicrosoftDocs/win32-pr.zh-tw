---
description: 目前的硬體不一定會執行 Direct3D 介面所啟用的所有功能。 您的應用程式必須測試使用者硬體，並據以調整其轉譯策略。
ms.assetid: 7b5f586c-616c-4351-b6b9-5c0179db5d8b
title: " (Direct3D 9) 進行紋理的硬體考慮"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41344d1ee091a1d2d619e366de549d58b69aebf234b89b6cf8115511703b799
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118522799"
---
# <a name="hardware-considerations-for-texturing-direct3d-9"></a> (Direct3D 9) 進行紋理的硬體考慮

目前的硬體不一定會執行 Direct3D 介面所啟用的所有功能。 您的應用程式必須測試使用者硬體，並據以調整其轉譯策略。

許多3D 加速器都不支援以擴散方式將反復的值當作混合單位的引數。 不過，您的應用程式可能會在執行材質混合時引進反復的色彩資料。

某些3D 硬體可能沒有與第一個材質相關聯的混合階段。 在這些介面卡上，您的應用程式必須在目前材質組的第二個和第三個材質階段中混合執行。

由於現今的大部分硬體都有限制，因此，少數顯示配接器可透過 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)所提供的多個紋理混合介面來執行三線性 mipmap 插補。 您的應用程式可以使用 multipass 材質混色來達成相同的效果，或降級為 D3DTEXF \_ 點 mipmap 篩選器模式，其受到廣泛支援。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 紋理](direct3d-textures.md)
</dt> </dl>

 

 
