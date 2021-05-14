---
description: 擴充 ShellLinkObject 物件，並支援一個額外的屬性。
title: 'IShellLinkDual2 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellLinkDual2
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 8a63552c-6bce-4583-8df8-a7f7731b35eb
ms.openlocfilehash: 47dc46d20fc6cf5096a38ccfd1790957f1fdd318
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842639"
---
# <a name="ishelllinkdual2-object"></a><span data-ttu-id="ea5f1-103">IShellLinkDual2 物件</span><span class="sxs-lookup"><span data-stu-id="ea5f1-103">IShellLinkDual2 object</span></span>

<span data-ttu-id="ea5f1-104">擴充 [**ShellLinkObject**](shelllinkobject-object.md) 物件，並支援一個額外的屬性。</span><span class="sxs-lookup"><span data-stu-id="ea5f1-104">Extends the [**ShellLinkObject**](shelllinkobject-object.md) object and supports one additional property.</span></span>

## <a name="members"></a><span data-ttu-id="ea5f1-105">成員</span><span class="sxs-lookup"><span data-stu-id="ea5f1-105">Members</span></span>

<span data-ttu-id="ea5f1-106">**IShellLinkDual2** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ea5f1-106">The **IShellLinkDual2** object has these types of members:</span></span>

-   [<span data-ttu-id="ea5f1-107">屬性</span><span class="sxs-lookup"><span data-stu-id="ea5f1-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ea5f1-108">屬性</span><span class="sxs-lookup"><span data-stu-id="ea5f1-108">Properties</span></span>

<span data-ttu-id="ea5f1-109">**IShellLinkDual2** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ea5f1-109">The **IShellLinkDual2** object has these properties.</span></span>



| <span data-ttu-id="ea5f1-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ea5f1-110">Property</span></span>                                            | <span data-ttu-id="ea5f1-111">存取類型</span><span class="sxs-lookup"><span data-stu-id="ea5f1-111">Access type</span></span>          | <span data-ttu-id="ea5f1-112">描述</span><span class="sxs-lookup"><span data-stu-id="ea5f1-112">Description</span></span>                                   |
|:----------------------------------------------------|:---------------------|:----------------------------------------------|
| [<span data-ttu-id="ea5f1-113">**目標**</span><span class="sxs-lookup"><span data-stu-id="ea5f1-113">**Target**</span></span>](ishelllinkdual2-target.md)<br/> | <span data-ttu-id="ea5f1-114">唯讀</span><span class="sxs-lookup"><span data-stu-id="ea5f1-114">Read-only</span></span><br/> | <span data-ttu-id="ea5f1-115">包含連結化物件的目標。</span><span class="sxs-lookup"><span data-stu-id="ea5f1-115">Contains the link object's target.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ea5f1-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea5f1-116">Requirements</span></span>



| <span data-ttu-id="ea5f1-117">需求</span><span class="sxs-lookup"><span data-stu-id="ea5f1-117">Requirement</span></span> | <span data-ttu-id="ea5f1-118">值</span><span class="sxs-lookup"><span data-stu-id="ea5f1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea5f1-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ea5f1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ea5f1-120">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea5f1-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea5f1-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ea5f1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ea5f1-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea5f1-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ea5f1-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ea5f1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea5f1-124"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="ea5f1-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ea5f1-125">Idl</span><span class="sxs-lookup"><span data-stu-id="ea5f1-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ea5f1-126"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ea5f1-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ea5f1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ea5f1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea5f1-128"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="ea5f1-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




