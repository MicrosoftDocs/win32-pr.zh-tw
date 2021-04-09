---
description: WMI 服務管理類別是用來管理 WMI 服務本身，而不是電腦系統或商業網路。 管理 WMI 包含設定 WMI 服務和管理 WMI 作業。
ms.assetid: EF58AC04-FE04-4D0C-A5F7-3491C885A0E4
ms.tgt_platform: multiple
title: WMI 服務管理類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502abebbddfd2ce90562045a8b0d7acd3974171
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110213"
---
# <a name="wmi-service-management-classes"></a><span data-ttu-id="0bc3d-104">WMI 服務管理類別</span><span class="sxs-lookup"><span data-stu-id="0bc3d-104">WMI Service Management Classes</span></span>

<span data-ttu-id="0bc3d-105">WMI 服務管理類別是用來管理 WMI 服務本身，而不是電腦系統或商業網路。</span><span class="sxs-lookup"><span data-stu-id="0bc3d-105">WMI service management classes are used to manage the WMI service itself and not the computer system or enterprise network.</span></span> <span data-ttu-id="0bc3d-106">管理 WMI 包含設定 WMI 服務和管理 WMI 作業。</span><span class="sxs-lookup"><span data-stu-id="0bc3d-106">Managing WMI encompasses both configuring the WMI service and managing WMI operations.</span></span>

<span data-ttu-id="0bc3d-107">WMI 服務管理類別包含下列類別的子類別：</span><span class="sxs-lookup"><span data-stu-id="0bc3d-107">The WMI Service Management category includes the following subcategories of classes:</span></span>

-   [<span data-ttu-id="0bc3d-108">WMI 設定類別</span><span class="sxs-lookup"><span data-stu-id="0bc3d-108">WMI configuration classes</span></span>](#wmi-configuration-classes)
-   [<span data-ttu-id="0bc3d-109">WMI 管理類別</span><span class="sxs-lookup"><span data-stu-id="0bc3d-109">WMI management classes</span></span>](#wmi-management-classes)

## <a name="wmi-configuration-classes"></a><span data-ttu-id="0bc3d-110">WMI 設定類別</span><span class="sxs-lookup"><span data-stu-id="0bc3d-110">WMI Configuration Classes</span></span>

<span data-ttu-id="0bc3d-111">WMI 設定類別會衍生設定 WMI 服務的方法。</span><span class="sxs-lookup"><span data-stu-id="0bc3d-111">The WMI Configuration class derives methods that configure the WMI service.</span></span>

<span data-ttu-id="0bc3d-112">以下是 WMI 設定類別的表格。</span><span class="sxs-lookup"><span data-stu-id="0bc3d-112">The following is a table of WMI configuration classes.</span></span>



| <span data-ttu-id="0bc3d-113">類別</span><span class="sxs-lookup"><span data-stu-id="0bc3d-113">Class</span></span>                                                             | <span data-ttu-id="0bc3d-114">描述</span><span class="sxs-lookup"><span data-stu-id="0bc3d-114">Description</span></span>                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="0bc3d-115">**Win32 \_ MethodParameterClass**</span><span class="sxs-lookup"><span data-stu-id="0bc3d-115">**Win32\_MethodParameterClass**</span></span>](win32-methodparameterclass.md) | <span data-ttu-id="0bc3d-116">抽象的基類，這個基類會實作為衍生自這個類別的方法參數。</span><span class="sxs-lookup"><span data-stu-id="0bc3d-116">Abstract, base class that implements method parameters derived from this class.</span></span> |



 

## <a name="wmi-management-classes"></a><span data-ttu-id="0bc3d-117">WMI 管理類別</span><span class="sxs-lookup"><span data-stu-id="0bc3d-117">WMI Management Classes</span></span>

<span data-ttu-id="0bc3d-118">WMI 管理類別代表 WMI 服務的指令引數。</span><span class="sxs-lookup"><span data-stu-id="0bc3d-118">The WMI management classes represent operational parameters for the WMI service.</span></span>

<span data-ttu-id="0bc3d-119">以下是 WMI 管理類別的表格。</span><span class="sxs-lookup"><span data-stu-id="0bc3d-119">The following is a table of WMI management classes.</span></span>



| <span data-ttu-id="0bc3d-120">類別</span><span class="sxs-lookup"><span data-stu-id="0bc3d-120">Class</span></span>                                                       | <span data-ttu-id="0bc3d-121">描述</span><span class="sxs-lookup"><span data-stu-id="0bc3d-121">Description</span></span>                                                                                   |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0bc3d-122">**Win32 \_ WMISetting**</span><span class="sxs-lookup"><span data-stu-id="0bc3d-122">**Win32\_WMISetting**</span></span>](win32-wmisetting.md)               | <span data-ttu-id="0bc3d-123">包含 WMI 服務的指令引數。</span><span class="sxs-lookup"><span data-stu-id="0bc3d-123">Contains the operational parameters for the WMI service.</span></span>                                      |
| [<span data-ttu-id="0bc3d-124">**Win32 \_ WMIElementSetting**</span><span class="sxs-lookup"><span data-stu-id="0bc3d-124">**Win32\_WMIElementSetting**</span></span>](win32-wmielementsetting.md) | <span data-ttu-id="0bc3d-125">在 Windows 系統中執行的服務與其可使用的 WMI 設定之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="0bc3d-125">Association between a service running in the Windows system, and the WMI settings it can use.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0bc3d-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="0bc3d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bc3d-127">Win32 類別</span><span class="sxs-lookup"><span data-stu-id="0bc3d-127">Win32 Classes</span></span>](./win32-provider.md)
</dt> </dl>

 

 
