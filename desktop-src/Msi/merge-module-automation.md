---
description: Mergemod.dll 提供的 COM 物件會針對合併模組執行合併作業和來源映射產生。 主要物件會針對 C/c + + 程式和自動化用戶端（包括 Visual Basic 和 VBScript）來實作為介面。
ms.assetid: 877d3691-948f-4aea-89d8-0ff008126ccc
title: 合併模組自動化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ae27370b2ad898cf9413567285afc41d117815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987403"
---
# <a name="merge-module-automation"></a><span data-ttu-id="ffe64-104">合併模組自動化</span><span class="sxs-lookup"><span data-stu-id="ffe64-104">Merge Module Automation</span></span>

<span data-ttu-id="ffe64-105">Mergemod.dll 提供的 COM 物件會針對合併模組執行合併作業和來源映射產生。</span><span class="sxs-lookup"><span data-stu-id="ffe64-105">Mergemod.dll provides a COM object that implements merge operations and source image generation for merge modules.</span></span> <span data-ttu-id="ffe64-106">主要物件會針對 C/c + + 程式和自動化用戶端（包括 Visual Basic 和 VBScript）來實作為介面。</span><span class="sxs-lookup"><span data-stu-id="ffe64-106">The main object implements interfaces for C/C++ programs and automation clients, including Visual Basic and VBScript.</span></span>

<span data-ttu-id="ffe64-107">安裝 Mergemod.dll 的慣用方法是使用 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="ffe64-107">The preferred method for installing Mergemod.dll is by using the Windows Installer.</span></span> <span data-ttu-id="ffe64-108">包含 Mergemod.dll COM 介面之元件的元件識別碼為 {FD153241-37EC-11D2-8892-00A0C981B015}。</span><span class="sxs-lookup"><span data-stu-id="ffe64-108">The Component ID for the component containing the Mergemod.dll COM interface is {FD153241-37EC-11D2-8892-00A0C981B015}.</span></span> <span data-ttu-id="ffe64-109">在所有 Windows 系統上都可以使用相同的二進位檔，而 dll 將會在舊版系統上透過 regsvr32 自行註冊。</span><span class="sxs-lookup"><span data-stu-id="ffe64-109">The same binary can be used on all Windows systems and the dll will self-register through regsvr32 on older systems.</span></span>

<span data-ttu-id="ffe64-110">請注意，Mergemod.dll 需要在系統上安裝 Msvcrt.dll。</span><span class="sxs-lookup"><span data-stu-id="ffe64-110">Note that Mergemod.dll requires that the Msvcrt.dll be installed on the system.</span></span>

<span data-ttu-id="ffe64-111">請注意，需要 Mergemod.dll 2.0 才能建立 [可設定的合併模組](configurable-merge-modules.md)。</span><span class="sxs-lookup"><span data-stu-id="ffe64-111">Note that Mergemod.dll 2.0 is required to create [Configurable Merge Modules](configurable-merge-modules.md).</span></span> <span data-ttu-id="ffe64-112">Mergemod.dll 版本2.0 會透過 [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) 介面在組建階段提供延伸的功能。</span><span class="sxs-lookup"><span data-stu-id="ffe64-112">Mergemod.dll version 2.0 provides extended functionality at build time through the [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) Interface.</span></span> <span data-ttu-id="ffe64-113">此 CLSID 支援 Mergemod.dll 版本1.0 所提供之 [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) 介面的所有現有功能。</span><span class="sxs-lookup"><span data-stu-id="ffe64-113">This CLSID supports all the existing functionality of the [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) Interface provided by Mergemod.dll version 1.0.</span></span> <span data-ttu-id="ffe64-114">Mergemod.dll 2.0 之 [**Merge**](merge-object.md) 物件的預設介面是 **IMsmMerge2** 介面，而不是 **IMsmMerge** 介面。</span><span class="sxs-lookup"><span data-stu-id="ffe64-114">The default interface on the [**Merge**](merge-object.md) object of Mergemod.dll 2.0 is the **IMsmMerge2** interface instead of the **IMsmMerge** interface.</span></span>

[<span data-ttu-id="ffe64-115">Mergemod.dll 版本1.0 的物件模型</span><span class="sxs-lookup"><span data-stu-id="ffe64-115">Object Model for Mergemod.dll Version 1.0</span></span>](object-model-for-mergemod-dll-version-1-0.md)

[<span data-ttu-id="ffe64-116">Mergemod.dll 版本2.0 的物件模型</span><span class="sxs-lookup"><span data-stu-id="ffe64-116">Object Model for Mergemod.dll Version 2.0</span></span>](object-model-for-mergemod-dll-version-2-0.md)

 

 
