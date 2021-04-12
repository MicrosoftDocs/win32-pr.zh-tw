---
description: 從 Windows 7 開始，Windows Management Instrumentation (WMI) 使用 CIM 架構來實行探索設定檔的標準機制。
ms.assetid: e748b623-5ff3-464d-ba09-96cf226de7b6
ms.tgt_platform: multiple
title: 跨命名空間關聯的遍歷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe2bbb408c4d89a7093adf45f3daf276df294ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848746"
---
# <a name="cross-namespace-association-traversal"></a><span data-ttu-id="4654a-103">跨命名空間關聯的遍歷</span><span class="sxs-lookup"><span data-stu-id="4654a-103">Cross-Namespace Association Traversal</span></span>

<span data-ttu-id="4654a-104">從 Windows 7 開始，Windows Management Instrumentation (WMI) 使用 CIM 架構來實行探索設定檔的標準機制。</span><span class="sxs-lookup"><span data-stu-id="4654a-104">Starting in Windows 7, Windows Management Instrumentation (WMI) implemented a standard mechanism for discovering profiles by using the CIM schema.</span></span>

<span data-ttu-id="4654a-105">WMI 支援跨命名空間關聯的遍歷和關聯設定檔註冊。</span><span class="sxs-lookup"><span data-stu-id="4654a-105">WMI supports the cross-namespace association traversal and association profile registration.</span></span> <span data-ttu-id="4654a-106">如需設定檔註冊和關聯性的 CIM 標準執行的詳細資訊，請參閱 DSP1033 ([https://www.dmtf.org/standards/published\_documents/DSP1033.pdf](https://www.dmtf.org/sites/default/files/standards/documents/DSP1033_1.0.0.pdf)) </span><span class="sxs-lookup"><span data-stu-id="4654a-106">For more information about profile registration and the CIM standard implementation of association traversal, see DSP1033 ([https://www.dmtf.org/standards/published\_documents/DSP1033.pdf](https://www.dmtf.org/sites/default/files/standards/documents/DSP1033_1.0.0.pdf))</span></span>

<span data-ttu-id="4654a-107">為了支援這項功能，WMI 基礎結構會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="4654a-107">To support this feature, the WMI infrastructure did the following:</span></span>

-   <span data-ttu-id="4654a-108">建立 interop 命名空間： \\ 根 \\ interop。</span><span class="sxs-lookup"><span data-stu-id="4654a-108">Created the interop namespace: \\root\\interop.</span></span>
-   <span data-ttu-id="4654a-109">允許的跨命名空間關聯遍歷。</span><span class="sxs-lookup"><span data-stu-id="4654a-109">Allowed cross namespace association traversal.</span></span> <span data-ttu-id="4654a-110">跨命名空間的關聯支援在關聯類別層級和實命名空間層級進行篩選。</span><span class="sxs-lookup"><span data-stu-id="4654a-110">Associations that cross namespaces support filtering at the association class level and at the implemented namespace level.</span></span>
-   <span data-ttu-id="4654a-111">已新增 [**cim \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))、 [**cim \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)和 [**cim \_ ReferencedProfile**](cim-referencedprofile.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="4654a-111">Added the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)), [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile), and [**CIM\_ReferencedProfile**](cim-referencedprofile.md) classes.</span></span>
-   <span data-ttu-id="4654a-112">實作為2.17.1 相容性的 CIM 架構版本。</span><span class="sxs-lookup"><span data-stu-id="4654a-112">Implemented CIM Schema version 2.17.1 compatibility.</span></span> <span data-ttu-id="4654a-113">如需詳細資訊，請參閱 [CIM 架構相容性](cim-schema-compatibility.md)。</span><span class="sxs-lookup"><span data-stu-id="4654a-113">For more information, see [CIM Schema Compatibility](cim-schema-compatibility.md).</span></span>

## <a name="interop-namespace"></a><span data-ttu-id="4654a-114">Interop 命名空間</span><span class="sxs-lookup"><span data-stu-id="4654a-114">Interop Namespace</span></span>

<span data-ttu-id="4654a-115">Interop 命名空間提供一個共同的位置，讓用戶端應用程式探索電腦支援的所有設定檔。</span><span class="sxs-lookup"><span data-stu-id="4654a-115">The interop namespace provides a common location for a client application to discover all of the profiles that are supported on a computer.</span></span> <span data-ttu-id="4654a-116">設定檔可用於管理作業系統、存放裝置陣列或資料庫的各種層面。</span><span class="sxs-lookup"><span data-stu-id="4654a-116">Profiles can be used to manage various aspects of an operating system, storage array, or database.</span></span>

<span data-ttu-id="4654a-117">所有 interop 類別和物件都必須在根 \\ interop 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="4654a-117">All interop classes and objects must be defined in the root\\interop namespace.</span></span>

## <a name="cim-classes"></a><span data-ttu-id="4654a-118">CIM 類別</span><span class="sxs-lookup"><span data-stu-id="4654a-118">CIM Classes</span></span>

<span data-ttu-id="4654a-119">下列清單中所述的 CIM 類別支援跨命名空間關聯的遍歷。</span><span class="sxs-lookup"><span data-stu-id="4654a-119">The CIM classes described in the following list support cross-namespace association traversal.</span></span>

<dl> <dt>

<span data-ttu-id="4654a-120"><span id="CIM_RegisteredProfile"></span><span id="cim_registeredprofile"></span><span id="CIM_REGISTEREDPROFILE"></span>[**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4654a-120"><span id="CIM_RegisteredProfile"></span><span id="cim_registeredprofile"></span><span id="CIM_REGISTEREDPROFILE"></span>[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="4654a-121">用來識別公告為已執行的設定檔規格。</span><span class="sxs-lookup"><span data-stu-id="4654a-121">Used to identify the profile specification that is advertised as being implemented.</span></span> <span data-ttu-id="4654a-122">這個類別會指定包含設定檔名稱、組織以及符合規範之版本的資訊。</span><span class="sxs-lookup"><span data-stu-id="4654a-122">This class specifies information that includes the profile name, organization, and version with which the implementation is compliant.</span></span>

</dd> <dt>

<span data-ttu-id="4654a-123"><span id="CIM_ElementConformsToProfile"></span><span id="cim_elementconformstoprofile"></span><span id="CIM_ELEMENTCONFORMSTOPROFILE"></span>[**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)</span><span class="sxs-lookup"><span data-stu-id="4654a-123"><span id="CIM_ElementConformsToProfile"></span><span id="cim_elementconformstoprofile"></span><span id="CIM_ELEMENTCONFORMSTOPROFILE"></span>[**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)</span></span>
</dt> <dd>

<span data-ttu-id="4654a-124">用來將設定檔中所定義之管理專案的實例與 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) 類別建立關聯，以識別所要執行的特定設定檔規格。</span><span class="sxs-lookup"><span data-stu-id="4654a-124">Used to associate instances of management elements that are defined in profiles with the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) class that identifies the particular profile specifications that are implemented.</span></span>

</dd> <dt>

<span data-ttu-id="4654a-125"><span id="CIM_ReferencedProfile"></span><span id="cim_referencedprofile"></span><span id="CIM_REFERENCEDPROFILE"></span>[**CIM \_ ReferencedProfile**](cim-referencedprofile.md)</span><span class="sxs-lookup"><span data-stu-id="4654a-125"><span id="CIM_ReferencedProfile"></span><span id="cim_referencedprofile"></span><span id="CIM_REFERENCEDPROFILE"></span>[**CIM\_ReferencedProfile**](cim-referencedprofile.md)</span></span>
</dt> <dd>

<span data-ttu-id="4654a-126">用來表示設定檔之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="4654a-126">Used to represent the relationship between profiles.</span></span>

</dd> </dl>

## <a name="implementing-cross-namespace-association-traversal"></a><span data-ttu-id="4654a-127">執行跨命名空間關聯的遍歷</span><span class="sxs-lookup"><span data-stu-id="4654a-127">Implementing Cross-Namespace Association Traversal</span></span>

<span data-ttu-id="4654a-128">WMI 服務允許跨命名空間關聯的遍歷。</span><span class="sxs-lookup"><span data-stu-id="4654a-128">The WMI service allows cross-namespace association traversal.</span></span> <span data-ttu-id="4654a-129">WMI 提供用來註冊設定檔的 interop 命名空間，並將其與在不同命名空間中執行的設定檔產生關聯。</span><span class="sxs-lookup"><span data-stu-id="4654a-129">WMI provides the interop namespace for registering profiles and associating them with profiles that are implemented in different namespaces.</span></span> <span data-ttu-id="4654a-130">不過，若要使用關聯性遍歷，實作者必須在 interop 和已執行的命名空間中具現化設定檔類別。</span><span class="sxs-lookup"><span data-stu-id="4654a-130">However, to use association traversal, implementers must instantiate the profile classes both in the interop and in the implemented namespace.</span></span> <span data-ttu-id="4654a-131">如需詳細資訊，請參閱 [撰寫 Interop 的關聯提供者](writing-an-association-provider-for-interop.md)。</span><span class="sxs-lookup"><span data-stu-id="4654a-131">For more information, see [Writing an Association Provider for Interop](writing-an-association-provider-for-interop.md).</span></span>

<span data-ttu-id="4654a-132">在同一個管理環境內跨命名空間的關聯，必須同時具現化于 interop 和已執行的命名空間中。</span><span class="sxs-lookup"><span data-stu-id="4654a-132">Associations that cross namespaces within the same management environment must be instantiated in both the interop and implemented namespaces.</span></span> <span data-ttu-id="4654a-133">否則，關聯遍歷將無法運作。</span><span class="sxs-lookup"><span data-stu-id="4654a-133">Otherwise, association traversal will not work.</span></span> <span data-ttu-id="4654a-134">例如，power profile 關聯提供者必須向根/interop 和根/cimv2/power 命名空間進行註冊。</span><span class="sxs-lookup"><span data-stu-id="4654a-134">For example, the power profile association provider must be registered with both root/interop and root/cimv2/power namespaces.</span></span> <span data-ttu-id="4654a-135">關聯分析應該能夠從任一命名空間傳回另一個。</span><span class="sxs-lookup"><span data-stu-id="4654a-135">Association traversal should be able to occur from either namespace back to the other.</span></span> <span data-ttu-id="4654a-136">如需關聯的範例，請參閱 [存取 Interop 命名空間中的資料](accessing-data-in-the-interop-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="4654a-136">For examples of association traversal, see [Accessing Data in the Interop Namespace](accessing-data-in-the-interop-namespace.md).</span></span>

<span data-ttu-id="4654a-137">\* \* Windows Vista： \* \*</span><span class="sxs-lookup"><span data-stu-id="4654a-137">\*\*Windows Vista:  \*\*</span></span>

<span data-ttu-id="4654a-138">升級到 Windows 7 之後，如果有先前安裝在根/interop 命名空間中的 interop 裝置設定檔，則不會安裝任何 Windows 7 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4654a-138">After upgrading to Windows 7, if there are interop device profiles that were previously installed in the root/interop namespace, no Windows 7 profiles will be installed.</span></span> <span data-ttu-id="4654a-139">這些協力廠商設定檔物件會覆寫 Windows 7 interop 架構以維護功能。</span><span class="sxs-lookup"><span data-stu-id="4654a-139">These third-party profile objects overwrite Windows 7 interop schema to maintain functionality.</span></span> <span data-ttu-id="4654a-140">此外，也會記錄 WMI 應用程式事件識別碼5631。</span><span class="sxs-lookup"><span data-stu-id="4654a-140">Additionally, the WMI application event ID 5631 is recorded.</span></span>

<span data-ttu-id="4654a-141">若要取得 Windows 7 interop 設定檔，必須編譯 Windows 7 版本的 Interop. mof 檔案和相關的 MFL 檔。</span><span class="sxs-lookup"><span data-stu-id="4654a-141">To get the Windows 7 interop profiles, the Windows 7 version of the Interop.mof file and the related MFL files must be compiled.</span></span> <span data-ttu-id="4654a-142">如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="4654a-142">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4654a-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="4654a-143">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4654a-144">[**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4654a-144">[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4654a-145">**CIM \_ ElementConformsToProfile**</span><span class="sxs-lookup"><span data-stu-id="4654a-145">**CIM\_ElementConformsToProfile**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[<span data-ttu-id="4654a-146">**CIM \_ ReferencedProfile**</span><span class="sxs-lookup"><span data-stu-id="4654a-146">**CIM\_ReferencedProfile**</span></span>](cim-referencedprofile.md)
</dt> <dt>

[<span data-ttu-id="4654a-147">CIM 架構相容性</span><span class="sxs-lookup"><span data-stu-id="4654a-147">CIM Schema Compatibility</span></span>](cim-schema-compatibility.md)
</dt> <dt>

[<span data-ttu-id="4654a-148">撰寫 Interop 的關聯提供者</span><span class="sxs-lookup"><span data-stu-id="4654a-148">Writing an Association Provider for Interop</span></span>](writing-an-association-provider-for-interop.md)
</dt> <dt>

[<span data-ttu-id="4654a-149">存取 Interop 命名空間中的資料</span><span class="sxs-lookup"><span data-stu-id="4654a-149">Accessing Data in the Interop Namespace</span></span>](accessing-data-in-the-interop-namespace.md)
</dt> </dl>

 

 
