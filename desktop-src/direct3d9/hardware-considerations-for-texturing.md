---
description: 目前的硬體不一定會執行 Direct3D 介面所啟用的所有功能。 您的應用程式必須測試使用者硬體，並據以調整其轉譯策略。
ms.assetid: 7b5f586c-616c-4351-b6b9-5c0179db5d8b
title: " (Direct3D 9) 進行紋理的硬體考慮"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f1ba8bea85cc3657478767aac7c7ffc2abebbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845668"
---
# <a name="hardware-considerations-for-texturing-direct3d-9"></a><span data-ttu-id="efc48-104"> (Direct3D 9) 進行紋理的硬體考慮</span><span class="sxs-lookup"><span data-stu-id="efc48-104">Hardware Considerations for Texturing (Direct3D 9)</span></span>

<span data-ttu-id="efc48-105">目前的硬體不一定會執行 Direct3D 介面所啟用的所有功能。</span><span class="sxs-lookup"><span data-stu-id="efc48-105">Current hardware does not necessarily implement all the functionality that the Direct3D interface enables.</span></span> <span data-ttu-id="efc48-106">您的應用程式必須測試使用者硬體，並據以調整其轉譯策略。</span><span class="sxs-lookup"><span data-stu-id="efc48-106">Your application must test user hardware and adjust its rendering strategies accordingly.</span></span>

<span data-ttu-id="efc48-107">許多3D 加速器都不支援以擴散方式將反復的值當作混合單位的引數。</span><span class="sxs-lookup"><span data-stu-id="efc48-107">Many 3D accelerator cards do not support diffuse iterated values as arguments to blending units.</span></span> <span data-ttu-id="efc48-108">不過，您的應用程式可能會在執行材質混合時引進反復的色彩資料。</span><span class="sxs-lookup"><span data-stu-id="efc48-108">However, your application can introduce iterated color data when it performs texture blending.</span></span>

<span data-ttu-id="efc48-109">某些3D 硬體可能沒有與第一個材質相關聯的混合階段。</span><span class="sxs-lookup"><span data-stu-id="efc48-109">Some 3D hardware may not have a blending stage associated with the first texture.</span></span> <span data-ttu-id="efc48-110">在這些介面卡上，您的應用程式必須在目前材質組的第二個和第三個材質階段中混合執行。</span><span class="sxs-lookup"><span data-stu-id="efc48-110">On these adapters, your application must perform blending in the second and third texture stages in the set of current textures.</span></span>

<span data-ttu-id="efc48-111">由於現今的大部分硬體都有限制，因此，少數顯示配接器可透過 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)所提供的多個紋理混合介面來執行三線性 mipmap 插補。</span><span class="sxs-lookup"><span data-stu-id="efc48-111">Because of limitations in much of today's hardware, few display adapters can perform trilinear mipmap interpolation through the multiple texture blending interface offered by [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span> <span data-ttu-id="efc48-112">您的應用程式可以使用 multipass 材質混色來達成相同的效果，或降級為 D3DTEXF \_ 點 mipmap 篩選器模式，其受到廣泛支援。</span><span class="sxs-lookup"><span data-stu-id="efc48-112">Your application can use multipass texture blending to achieve the same effects, or degrade to the D3DTEXF\_POINT mipmap filter mode, which is widely supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="efc48-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="efc48-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efc48-114">Direct3D 紋理</span><span class="sxs-lookup"><span data-stu-id="efc48-114">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 
