---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 50397050-3b5c-4683-972c-95d9f661b365
ms.tgt_platform: multiple
title: 'D (WMI) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d469b94ec6649c64722fb414880d2e79fc3c88b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026854"
---
# <a name="d-wmi"></a><span data-ttu-id="46a1d-103">D (WMI) </span><span class="sxs-lookup"><span data-stu-id="46a1d-103">D (WMI)</span></span>

<span data-ttu-id="46a1d-104">[B](gloss-a.md) [C](gloss-c.md) D [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) [W](gloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="46a1d-104">[A](gloss-a.md) B [C](gloss-c.md) D [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="46a1d-105"><span id="wmi.gloss_datetime"></span><span id="WMI.GLOSS_DATETIME"></span>**Datetime**</span><span class="sxs-lookup"><span data-stu-id="46a1d-105"><span id="wmi.gloss_datetime"></span><span id="WMI.GLOSS_DATETIME"></span>**datetime**</span></span>
</dt> <dd>

<span data-ttu-id="46a1d-106">請參閱 [*CIM datetime*](gloss-c.md)。</span><span class="sxs-lookup"><span data-stu-id="46a1d-106">See [*CIM datetime*](gloss-c.md).</span></span>

</dd> <dt>

<span data-ttu-id="46a1d-107"><span id="wmi.gloss_decoupled_provider"></span><span id="WMI.GLOSS_DECOUPLED_PROVIDER"></span>**低耦合提供者**</span><span class="sxs-lookup"><span data-stu-id="46a1d-107"><span id="wmi.gloss_decoupled_provider"></span><span id="WMI.GLOSS_DECOUPLED_PROVIDER"></span>**decoupled provider**</span></span>
</dt> <dd>

<span data-ttu-id="46a1d-108">裝載在與 WMI 不同的處理序中的提供者。</span><span class="sxs-lookup"><span data-stu-id="46a1d-108">A provider hosted in a separate process from WMI.</span></span> <span data-ttu-id="46a1d-109">由於提供者可以控制其本身的存留期，而不是每次使用者透過 WMI 存取提供者時啟動，因此建議使用低耦合提供者來檢測應用程式。</span><span class="sxs-lookup"><span data-stu-id="46a1d-109">Decoupled providers are the recommended way to instrument an application, because the provider can control its own lifetime instead of being started each time a user accesses the provider through WMI.</span></span>

</dd> <dt>

<span data-ttu-id="46a1d-110"><span id="wmi.gloss_direct_access"></span><span id="WMI.GLOSS_DIRECT_ACCESS"></span>**直接存取**</span><span class="sxs-lookup"><span data-stu-id="46a1d-110"><span id="wmi.gloss_direct_access"></span><span id="WMI.GLOSS_DIRECT_ACCESS"></span>**direct access**</span></span>
</dt> <dd>

<span data-ttu-id="46a1d-111">在腳本中存取 WMI 提供的屬性和方法，就像是 [**SWbemObject**](swbemobject.md)的 automation 屬性和方法一樣。</span><span class="sxs-lookup"><span data-stu-id="46a1d-111">A way to access properties and methods supplied by WMI in a script as if they were automation properties and methods of [**SWbemObject**](swbemobject.md).</span></span>

<span data-ttu-id="46a1d-112">Nondirect 存取： `VolumeName = MyDisk.Properties_("VolumeName")`</span><span class="sxs-lookup"><span data-stu-id="46a1d-112">Nondirect access: `VolumeName = MyDisk.Properties_("VolumeName")`</span></span>

<span data-ttu-id="46a1d-113">直接存取： `VolumeName = MyDisk.VolumeName`</span><span class="sxs-lookup"><span data-stu-id="46a1d-113">Direct access: `VolumeName = MyDisk.VolumeName`</span></span>

</dd> <dt>

<span data-ttu-id="46a1d-114"><span id="wmi.gloss_distributed_management_task_force"></span><span id="WMI.GLOSS_DISTRIBUTED_MANAGEMENT_TASK_FORCE"></span>**分散式管理工作強制 (DMTF)**</span><span class="sxs-lookup"><span data-stu-id="46a1d-114"><span id="wmi.gloss_distributed_management_task_force"></span><span id="WMI.GLOSS_DISTRIBUTED_MANAGEMENT_TASK_FORCE"></span>**Distributed Management Task Force (DMTF)**</span></span>
</dt> <dd>

<span data-ttu-id="46a1d-115">適用于重要技術廠商（包括 Microsoft）的國際標準組織，可領導開發、採用和統一桌面、企業和網際網路環境的管理標準和計畫。</span><span class="sxs-lookup"><span data-stu-id="46a1d-115">An international standards organization that works with key technology vendors, including Microsoft, to lead the development, adoption, and unification of management standards and initiatives for desktop, enterprise, and Internet environments.</span></span>

</dd> <dt>

<span data-ttu-id="46a1d-116"><span id="wmi.gloss_dmtf"></span><span id="WMI.GLOSS_DMTF"></span>**DMTF**</span><span class="sxs-lookup"><span data-stu-id="46a1d-116"><span id="wmi.gloss_dmtf"></span><span id="WMI.GLOSS_DMTF"></span>**DMTF**</span></span>
</dt> <dd>

<span data-ttu-id="46a1d-117">請參閱 *分散式管理工作強制 (DMTF)*。</span><span class="sxs-lookup"><span data-stu-id="46a1d-117">See *Distributed Management Task Force (DMTF)*.</span></span>

</dd> <dt>

<span data-ttu-id="46a1d-118"><span id="wmi.gloss_dynamic_class"></span><span id="WMI.GLOSS_DYNAMIC_CLASS"></span>**動態類別**</span><span class="sxs-lookup"><span data-stu-id="46a1d-118"><span id="wmi.gloss_dynamic_class"></span><span id="WMI.GLOSS_DYNAMIC_CLASS"></span>**dynamic class**</span></span>
</dt> <dd>

<span data-ttu-id="46a1d-119">CIM 類別，其定義是由 [*提供者*](gloss-p.md) 在執行時間依需要提供。</span><span class="sxs-lookup"><span data-stu-id="46a1d-119">A CIM class whose definition is supplied by a [*provider*](gloss-p.md) at run time, as required.</span></span> <span data-ttu-id="46a1d-120">動態類別代表提供者特定的 [*managed 物件*](gloss-m.md) ，而且不會儲存在 [*CIM 存放庫*](gloss-c.md)中。</span><span class="sxs-lookup"><span data-stu-id="46a1d-120">Dynamic classes represent provider-specific [*managed objects*](gloss-m.md) and are not stored in the [*CIM repository*](gloss-c.md).</span></span> <span data-ttu-id="46a1d-121">動態類別僅支援 *動態實例*。</span><span class="sxs-lookup"><span data-stu-id="46a1d-121">Dynamic classes support only *dynamic instances*.</span></span>

</dd> <dt>

<span data-ttu-id="46a1d-122"><span id="wmi.gloss_dynamic_instance"></span><span id="WMI.GLOSS_DYNAMIC_INSTANCE"></span>**動態實例**</span><span class="sxs-lookup"><span data-stu-id="46a1d-122"><span id="wmi.gloss_dynamic_instance"></span><span id="WMI.GLOSS_DYNAMIC_INSTANCE"></span>**dynamic instance**</span></span>
</dt> <dd>

<span data-ttu-id="46a1d-123">當需要時， [*提供者*](gloss-p.md) 所提供之 CIM 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="46a1d-123">An instance of a CIM class that is supplied by a [*provider*](gloss-p.md) when required.</span></span> <span data-ttu-id="46a1d-124">它不會儲存在 [*CIM 存放庫*](gloss-c.md)中。</span><span class="sxs-lookup"><span data-stu-id="46a1d-124">It is not stored in the [*CIM repository*](gloss-c.md).</span></span> <span data-ttu-id="46a1d-125">可以為靜態或動態類別提供動態實例。</span><span class="sxs-lookup"><span data-stu-id="46a1d-125">Dynamic instances can be provided for either static or dynamic classes.</span></span> <span data-ttu-id="46a1d-126">動態支援類別的實例可讓提供者提供最新的 [*屬性*](gloss-p.md) 值。</span><span class="sxs-lookup"><span data-stu-id="46a1d-126">Dynamically supporting instances of a class enables a provider to supply up-to-the-minute [*property*](gloss-p.md) values.</span></span>

</dd> </dl>

 

 



