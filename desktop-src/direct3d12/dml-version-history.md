---
title: DirectML 版本歷程記錄
description: DirectML 是以 Windows 10 的系統元件的形式散發，並可作為 windows 10 作業系統) windows 10 1903 版 (10.0; 中的 Windows 10 作業系統 (作業系統。組建 18362) 和更新版本。
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 04cb7a2c906d7674c793a9a99e21609ea874dbc1
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104548477"
---
# <a name="directml-version-history"></a><span data-ttu-id="64def-103">DirectML 版本歷程記錄</span><span class="sxs-lookup"><span data-stu-id="64def-103">DirectML version history</span></span>

<span data-ttu-id="64def-104">DirectML 是以 Windows 10 的系統元件的形式散發，並可作為 windows 10 作業系統) windows 10 1903 版 (10.0; 中的 Windows 10 作業系統 (作業系統。組建 18362) 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="64def-104">DirectML is distributed as a system component of Windows 10, and is available as part of the Windows 10 operating system (OS) in Windows 10, version 1903 (10.0; Build 18362), and newer.</span></span>

<span data-ttu-id="64def-105">從 DirectML 版本1.4.0 開始，DirectML 也可做為獨立的可轉散發套件， (查看 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)) ，此功能適用于想要使用固定版本 DirectML 的應用程式，或在舊版 Windows 10 上執行時。</span><span class="sxs-lookup"><span data-stu-id="64def-105">Starting with DirectML version 1.4.0, DirectML is also available as a standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)), which is useful for applications that wish to use a fixed version of DirectML, or when running on older versions of Windows 10.</span></span>

<span data-ttu-id="64def-106">DirectML 遵循 [語義版本](https://semver.org/) 設定慣例。</span><span class="sxs-lookup"><span data-stu-id="64def-106">DirectML follows the [semantic versioning](https://semver.org/) conventions.</span></span> <span data-ttu-id="64def-107">亦即，版本號碼會遵循表單 `major.minor.patch` 。</span><span class="sxs-lookup"><span data-stu-id="64def-107">That is, version numbers follow the form `major.minor.patch`.</span></span> <span data-ttu-id="64def-108">DirectML 的第一個版本有1.0.0 版。</span><span class="sxs-lookup"><span data-stu-id="64def-108">The first release of DirectML has a version of 1.0.0.</span></span>

## <a name="version-table"></a><span data-ttu-id="64def-109">版本資料表</span><span class="sxs-lookup"><span data-stu-id="64def-109">Version table</span></span>

|<span data-ttu-id="64def-110">DirectML 版本</span><span class="sxs-lookup"><span data-stu-id="64def-110">DirectML version</span></span>|<span data-ttu-id="64def-111">支援的功能層級 (參閱 [DirectML 功能層級歷程記錄](./dml-feature-level-history.md)) </span><span class="sxs-lookup"><span data-stu-id="64def-111">Feature level supported (see [DirectML feature level history](./dml-feature-level-history.md))</span></span>|<span data-ttu-id="64def-112">DML_TARGET_VERSION</span><span class="sxs-lookup"><span data-stu-id="64def-112">DML_TARGET_VERSION</span></span>|<span data-ttu-id="64def-113">首次提供</span><span class="sxs-lookup"><span data-stu-id="64def-113">First available in</span></span>|<span data-ttu-id="64def-114"> (可轉散發套件中的第一版) </span><span class="sxs-lookup"><span data-stu-id="64def-114">First available in (Redistributable)</span></span>|
|-|-|-|-|-|-|
|<span data-ttu-id="64def-115">1.4.0<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="64def-115">1.4.0<sup>1</sup></span></span>|<span data-ttu-id="64def-116">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="64def-116">DML_FEATURE_LEVEL_3_0</span></span>|`0x3000`|<span data-ttu-id="64def-117">N/A</span><span class="sxs-lookup"><span data-stu-id="64def-117">N/A</span></span>|[<span data-ttu-id="64def-118">DirectML-1.4。0</span><span class="sxs-lookup"><span data-stu-id="64def-118">DirectML-1.4.0</span></span>](https://www.nuget.org/packages/Microsoft.AI.DirectML/)|
|<span data-ttu-id="64def-119">1.1.0</span><span class="sxs-lookup"><span data-stu-id="64def-119">1.1.0</span></span>|<span data-ttu-id="64def-120">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="64def-120">DML_FEATURE_LEVEL_2_0</span></span>|`0x2000`|<span data-ttu-id="64def-121">Windows 10 2004 版 (10.0;組建 19041)  (Windows 10 2020 版更新) 。</span><span class="sxs-lookup"><span data-stu-id="64def-121">Windows 10, version 2004 (10.0; Build 19041) (Windows 10 May 2020 Update).</span></span> <span data-ttu-id="64def-122">也稱為「20H1」。</span><span class="sxs-lookup"><span data-stu-id="64def-122">Aka "20H1".</span></span>|<span data-ttu-id="64def-123">N/A</span><span class="sxs-lookup"><span data-stu-id="64def-123">N/A</span></span>|
|<span data-ttu-id="64def-124">1.0.0</span><span class="sxs-lookup"><span data-stu-id="64def-124">1.0.0</span></span>|<span data-ttu-id="64def-125">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="64def-125">DML_FEATURE_LEVEL_1_0</span></span>|`0x1000`|<span data-ttu-id="64def-126">Windows 10 1903 版 (10.0;組建 18362)  (Windows 10 2019 版更新) 。</span><span class="sxs-lookup"><span data-stu-id="64def-126">Windows 10, version 1903 (10.0; Build 18362) (Windows 10 May 2019 Update).</span></span> <span data-ttu-id="64def-127">也稱為「19H1」。</span><span class="sxs-lookup"><span data-stu-id="64def-127">Aka "19H1".</span></span>|<span data-ttu-id="64def-128">N/A</span><span class="sxs-lookup"><span data-stu-id="64def-128">N/A</span></span>|

<span data-ttu-id="64def-129"><sup>1</sup> 1.2.0 和1.3.0 中繼版本的 DirectML 未提供廣泛的支援。</span><span class="sxs-lookup"><span data-stu-id="64def-129"><sup>1</sup> The 1.2.0 and 1.3.0 intermediate releases of DirectML weren't made widely available.</span></span>

## <a name="selecting-a-directml-target-version"></a><span data-ttu-id="64def-130">選取 DirectML 目標版本</span><span class="sxs-lookup"><span data-stu-id="64def-130">Selecting a DirectML target version</span></span>

<span data-ttu-id="64def-131">為了方便起見，標頭檔中的某些功能 `DirectML.h` 會根據宏的值，有條件地宣告 `DML_TARGET_VERSION` 。</span><span class="sxs-lookup"><span data-stu-id="64def-131">For convenience, certain features in the `DirectML.h` header file are declared conditionally based on the value of the `DML_TARGET_VERSION` macro.</span></span> <span data-ttu-id="64def-132">藉由將 `DML_TARGET_VERSION` 宏設定為特定值，您可以 `DirectML.h` 從應用程式中排除的部分。</span><span class="sxs-lookup"><span data-stu-id="64def-132">By setting the `DML_TARGET_VERSION` macro to certain values, you can exclude parts of `DirectML.h` from your application.</span></span>

<span data-ttu-id="64def-133">如果您使用較新的 `DirectML.h` 版本，但您的目標是較低版本的 DirectML 二進位檔，這會很有説明，因為它可確保任何嘗試使用所選目標層以外的功能都不會進行編譯。</span><span class="sxs-lookup"><span data-stu-id="64def-133">That can be helpful if you're using a newer copy of `DirectML.h`, but you're targeting a lower version of the DirectML binary, because it ensures that any attempt to use features beyond the chosen target level won't compile.</span></span> <span data-ttu-id="64def-134">這個機制類似于 `NTDDI_VERSION` 宏 (請參閱) [條件式宣告的宏](../winprog/using-the-windows-headers.md#macros-for-conditional-declarations) 。</span><span class="sxs-lookup"><span data-stu-id="64def-134">This mechanism is similar to the `NTDDI_VERSION` macro (see [Macros for conditional declarations](../winprog/using-the-windows-headers.md#macros-for-conditional-declarations)).</span></span>

<span data-ttu-id="64def-135">以下是宏的有效值 `DML_TARGET_VERSION` 。</span><span class="sxs-lookup"><span data-stu-id="64def-135">Here are the valid values for the `DML_TARGET_VERSION` macro.</span></span>

|<span data-ttu-id="64def-136">DML_TARGET_VERSION</span><span class="sxs-lookup"><span data-stu-id="64def-136">DML_TARGET_VERSION</span></span>|<span data-ttu-id="64def-137">效果</span><span class="sxs-lookup"><span data-stu-id="64def-137">Effect</span></span>|
|-|-|
|`0x3000`|<span data-ttu-id="64def-138">任何需要比 **1.4.0** 更新之 DirectML 版本的功能，都將從中排除 `DirectML.h` 。</span><span class="sxs-lookup"><span data-stu-id="64def-138">Any features that require a version of DirectML newer than **1.4.0** are excluded from `DirectML.h`.</span></span>|
|`0x2000`|<span data-ttu-id="64def-139">任何需要比 **1.1.0** 更新之 DirectML 版本的功能，都將從中排除 `DirectML.h` 。</span><span class="sxs-lookup"><span data-stu-id="64def-139">Any features that require a version of DirectML newer than **1.1.0** are excluded from `DirectML.h`.</span></span>|
|`0x1000`|<span data-ttu-id="64def-140">任何需要比 **1.0.0** 版 DirectML 更新的功能都會從排除 `DirectML.h` 。</span><span class="sxs-lookup"><span data-stu-id="64def-140">Any features that require a version of DirectML newer than **1.0.0** are excluded from `DirectML.h`.</span></span>|
|<span data-ttu-id="64def-141">*未設定*</span><span class="sxs-lookup"><span data-stu-id="64def-141">*Not set*</span></span>|<span data-ttu-id="64def-142">系統會自動為您選取目標版本。</span><span class="sxs-lookup"><span data-stu-id="64def-142">The target version is selected automatically for you.</span></span> <span data-ttu-id="64def-143">如需詳細資料，請參閱下文。</span><span class="sxs-lookup"><span data-stu-id="64def-143">See below for details.</span></span>|

<span data-ttu-id="64def-144">如果 `DML_TARGET_VERSION` 未設定，則會自動選取它，如下所示。</span><span class="sxs-lookup"><span data-stu-id="64def-144">If `DML_TARGET_VERSION` is not set, then it is selected automatically by the following.</span></span>

* <span data-ttu-id="64def-145">如果已 `DML_TARGET_VERSION_USE_LATEST` 定義宏，則會選取最新的目標版本。</span><span class="sxs-lookup"><span data-stu-id="64def-145">If the `DML_TARGET_VERSION_USE_LATEST` macro is defined, then the latest target version is selected.</span></span>
* <span data-ttu-id="64def-146">否則，會根據宏的值選取目標版本 `NTDDI_VERSION` 。</span><span class="sxs-lookup"><span data-stu-id="64def-146">Otherwise, the target version is selected based on the value of the `NTDDI_VERSION` macro.</span></span>
  *  <span data-ttu-id="64def-147">`NTDDI_WIN10_19H1` 產生的目標版本 `0x1000` 。</span><span class="sxs-lookup"><span data-stu-id="64def-147">`NTDDI_WIN10_19H1` results in a target version of `0x1000`.</span></span>
  *  <span data-ttu-id="64def-148">`NTDDI_WIN10_VB` 產生的目標版本 `0x2000` 。</span><span class="sxs-lookup"><span data-stu-id="64def-148">`NTDDI_WIN10_VB` results in a target version of `0x2000`.</span></span>
  *  <span data-ttu-id="64def-149">如果 `NTDDI_VERSION` 未定義，則會選取最新的目標版本， (如同 `DML_TARGET_VERSION_USE_LATEST`) 指定。</span><span class="sxs-lookup"><span data-stu-id="64def-149">If `NTDDI_VERSION` is not defined, then the latest target version is selected (as if `DML_TARGET_VERSION_USE_LATEST` were specified).</span></span>

### <a name="example"></a><span data-ttu-id="64def-150">範例</span><span class="sxs-lookup"><span data-stu-id="64def-150">Example</span></span>

<span data-ttu-id="64def-151">請考慮使用版本 10.0.19041.0 (Windows 10) 2004 版 windows 軟體發展工具組 (SDK) 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="64def-151">Consider an application using version 10.0.19041.0 (Windows 10, version 2004) of the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="64def-152">從上表中，這個對應的 DirectML 版本是1.1.0，而對應的 `DML_TARGET_VERSION` 是 `0x2000` 。</span><span class="sxs-lookup"><span data-stu-id="64def-152">From the table above, the version of DirectML that this corresponds to is 1.1.0, and the corresponding `DML_TARGET_VERSION` is `0x2000`.</span></span>

<span data-ttu-id="64def-153">如果您未設定 `DML_TARGET_VERSION` 或 `NTDDI_VERSION` 宏，則選取的目標版本將預設為 `0x2000` ，而且中的所有專案都可供 `DirectML.h` 使用。</span><span class="sxs-lookup"><span data-stu-id="64def-153">If you don't set either the `DML_TARGET_VERSION` nor the `NTDDI_VERSION` macros, then the selected target version will default to `0x2000`, and everything in `DirectML.h` will be available for use.</span></span>

<span data-ttu-id="64def-154">如果您想要讓應用程式能夠在 Windows 10 上執行，1903版 (10.0;組建 18362) ，然後您就可以 `#define DML_TARGET_VERSION 0x1000` 將 `DirectML.h` DirectML 1.0.0 版不支援的所有內容排除在其中。</span><span class="sxs-lookup"><span data-stu-id="64def-154">If you want your application to be able to run on Windows 10, version 1903 (10.0; Build 18362), then you could `#define DML_TARGET_VERSION 0x1000`, which will exclude all content in `DirectML.h` that isn't supported by DirectML version 1.0.0.</span></span> <span data-ttu-id="64def-155">這可確保任何嘗試使用需要較高版本之功能的嘗試都將無法編譯。</span><span class="sxs-lookup"><span data-stu-id="64def-155">This ensures that any attempt to use functionality that requires a greater version will fail to compile.</span></span>

## <a name="directml-version-versus-feature-level"></a><span data-ttu-id="64def-156">DirectML 版本與功能等級</span><span class="sxs-lookup"><span data-stu-id="64def-156">DirectML version versus feature level</span></span>

<span data-ttu-id="64def-157">DirectML 版本 (例如，1.0.0 或 1.4.0) 說明特定版本的 DirectML，包括其相關聯的 `DirectML.h` 標頭檔和檔案 `.lib` 。</span><span class="sxs-lookup"><span data-stu-id="64def-157">The DirectML version (for example, 1.0.0, or 1.4.0) describes a particular release of DirectML, including its associated `DirectML.h` header file and `.lib` file.</span></span>

<span data-ttu-id="64def-158">例如，或) 的功能層級 (`DML_FEATURE_LEVEL_1_0` `DML_FEATURE_LEVEL_2_0` 描述 API 基礎執行的功能，這可能會因使用的版本而異 `DirectML.h` 。</span><span class="sxs-lookup"><span data-stu-id="64def-158">The feature level (for example, `DML_FEATURE_LEVEL_1_0`, or `DML_FEATURE_LEVEL_2_0`) describes the capability of the underlying implementation of the API, which can vary from the version of `DirectML.h` used.</span></span>

<span data-ttu-id="64def-159">例如，針對較新的 SDK 所建立，但在舊版 Windows 上執行的應用程式，可能會在執行時間 () 查看較低支援的功能層級，即使是針對最新的 SDK 進行編譯也一樣。</span><span class="sxs-lookup"><span data-stu-id="64def-159">For example, an application building against a newer SDK, but running on an older version of Windows, might (at runtime) see a lower supported feature level, even if it's compiled against the latest SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="64def-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64def-160">See also</span></span>

<span data-ttu-id="64def-161">[DirectML 功能等級歷程記錄](./dml-feature-level-history.md) 
[DML_FEATURE_LEVEL 列舉](/windows/win32/api/directml/ne-directml-dml_feature_level) 
[DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="64def-161">[DirectML feature level history](./dml-feature-level-history.md)
[DML_FEATURE_LEVEL enumeration](/windows/win32/api/directml/ne-directml-dml_feature_level)
[Microsoft.AI.DirectML redistributable package](https://www.nuget.org/packages/Microsoft.AI.DirectML/)</span></span>