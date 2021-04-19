---
description: Win32 \_ QuickFixEngineering&\# 8194;WMI 類別代表小規模的全系統更新，通常稱為快速修正工程 (QFE) 更新，套用至目前的作業系統。
ms.assetid: 84aed428-7620-4f7a-941f-f9d683020d8a
ms.tgt_platform: multiple
title: Win32_QuickFixEngineering 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_QuickFixEngineering
- Win32_QuickFixEngineering.Caption
- Win32_QuickFixEngineering.Description
- Win32_QuickFixEngineering.InstallDate
- Win32_QuickFixEngineering.Name
- Win32_QuickFixEngineering.Status
- Win32_QuickFixEngineering.CSName
- Win32_QuickFixEngineering.FixComments
- Win32_QuickFixEngineering.HotFixID
- Win32_QuickFixEngineering.InstalledBy
- Win32_QuickFixEngineering.InstalledOn
- Win32_QuickFixEngineering.ServicePackInEffect
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0e9db31dd452161a31575b6f7184a34c35dea71e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970905"
---
# <a name="win32_quickfixengineering-class"></a><span data-ttu-id="a418a-103">Win32 \_ QuickFixEngineering 類別</span><span class="sxs-lookup"><span data-stu-id="a418a-103">Win32\_QuickFixEngineering class</span></span>

<span data-ttu-id="a418a-104">**Win32 \_ QuickFixEngineering** [WMI 類別](../wmisdk/retrieving-a-class.md)代表小規模的全系統更新，通常稱為快速修正工程 (QFE) 更新，套用至目前的作業系統。</span><span class="sxs-lookup"><span data-stu-id="a418a-104">The **Win32\_QuickFixEngineering** [WMI class](../wmisdk/retrieving-a-class.md) represents a small system-wide update, commonly referred to as a quick-fix engineering (QFE) update, applied to the current operating system.</span></span> <span data-ttu-id="a418a-105">這個類別只會傳回以元件為基礎的服務 (CBS) 所提供的更新。</span><span class="sxs-lookup"><span data-stu-id="a418a-105">This class returns only the updates supplied by Component Based Servicing (CBS).</span></span> <span data-ttu-id="a418a-106">這些更新不會列在登錄中。</span><span class="sxs-lookup"><span data-stu-id="a418a-106">These updates are not listed in the registry.</span></span> <span data-ttu-id="a418a-107">[https://update.microsoft.com](https://update.microsoft.com/) **Win32 \_ QuickFixEngineering** 不會傳回 Microsoft Windows Installer (MSI) 或 Windows update 網站 () 所提供的更新。</span><span class="sxs-lookup"><span data-stu-id="a418a-107">Updates supplied by Microsoft Windows Installer (MSI) or the Windows update site ([https://update.microsoft.com](https://update.microsoft.com/)) are not returned by **Win32\_QuickFixEngineering**.</span></span>

<span data-ttu-id="a418a-108">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a418a-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a418a-109">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="a418a-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a418a-110">語法</span><span class="sxs-lookup"><span data-stu-id="a418a-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0827250D-BA3E-11d2-B361-00105A1F77A1}"), AMENDMENT]
class Win32_QuickFixEngineering : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CSName;
  string   FixComments;
  string   HotFixID;
  string   InstalledBy;
  string   InstalledOn;
  string   ServicePackInEffect;
};
```

## <a name="members"></a><span data-ttu-id="a418a-111">成員</span><span class="sxs-lookup"><span data-stu-id="a418a-111">Members</span></span>

<span data-ttu-id="a418a-112">**Win32 \_ QuickFixEngineering** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a418a-112">The **Win32\_QuickFixEngineering** class has these types of members:</span></span>

-   [<span data-ttu-id="a418a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="a418a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a418a-114">屬性</span><span class="sxs-lookup"><span data-stu-id="a418a-114">Properties</span></span>

<span data-ttu-id="a418a-115">**Win32 \_ QuickFixEngineering** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a418a-115">The **Win32\_QuickFixEngineering** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a418a-116">**標題**</span><span class="sxs-lookup"><span data-stu-id="a418a-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a418a-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a418a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a418a-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a418a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a418a-119">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="a418a-119">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a418a-120">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="a418a-120">A short textual description of the object.</span></span>

<span data-ttu-id="a418a-121">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a418a-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a418a-122">**CSName**</span><span class="sxs-lookup"><span data-stu-id="a418a-122">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a418a-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a418a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a418a-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a418a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a418a-125">限定詞： [**cim \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) ， [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**cim \_**](cim-computersystem.md)未產生」。**Name**") ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" WMI ") </span><span class="sxs-lookup"><span data-stu-id="a418a-125">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="a418a-126">電腦系統的本機名稱。</span><span class="sxs-lookup"><span data-stu-id="a418a-126">Local name of the computer system.</span></span> <span data-ttu-id="a418a-127">這個屬性的值來自 CIM 的工作 [**類型 \_**](cim-computersystem.md) 。</span><span class="sxs-lookup"><span data-stu-id="a418a-127">The value for this property comes from the [**CIM\_ComputerSystem**](cim-computersystem.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="a418a-128">**說明**</span><span class="sxs-lookup"><span data-stu-id="a418a-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a418a-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a418a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a418a-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a418a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a418a-131">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="a418a-131">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a418a-132">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="a418a-132">A textual description of the object.</span></span>

<span data-ttu-id="a418a-133">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a418a-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a418a-134">**FixComments**</span><span class="sxs-lookup"><span data-stu-id="a418a-134">**FixComments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a418a-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a418a-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a418a-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a418a-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a418a-137">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SOFTWARE \\ \\ Microsoft \\ \\ Windows NT CurrentVersion 的修正 \\ \\ \\ \\ 程式" ) </span><span class="sxs-lookup"><span data-stu-id="a418a-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="a418a-138">與更新相關的其他批註。</span><span class="sxs-lookup"><span data-stu-id="a418a-138">Additional comments that relate to the update.</span></span>

</dd> <dt>

<span data-ttu-id="a418a-139">**HotFixID**</span><span class="sxs-lookup"><span data-stu-id="a418a-139">**HotFixID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a418a-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a418a-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a418a-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a418a-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a418a-142">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (260) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SOFTWARE \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ " ) </span><span class="sxs-lookup"><span data-stu-id="a418a-142">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="a418a-143">與特定更新相關聯的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="a418a-143">Unique identifier associated with a particular update.</span></span>

</dd> <dt>

<span data-ttu-id="a418a-144">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a418a-144">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a418a-145">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="a418a-145">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a418a-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a418a-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a418a-147">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="a418a-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a418a-148">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="a418a-148">Indicates when the object was installed.</span></span> <span data-ttu-id="a418a-149">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="a418a-149">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a418a-150">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a418a-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a418a-151">**InstalledBy**</span><span class="sxs-lookup"><span data-stu-id="a418a-151">**InstalledBy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a418a-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a418a-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a418a-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a418a-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a418a-154">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SOFTWARE \\ \\ Microsoft \\ \\ Windows NT CurrentVersion 的修正 \\ \\ \\ \\ 程式" ) </span><span class="sxs-lookup"><span data-stu-id="a418a-154">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="a418a-155">安裝更新的人員。</span><span class="sxs-lookup"><span data-stu-id="a418a-155">Person who installed the update.</span></span> <span data-ttu-id="a418a-156">如果這個值是未知的，則屬性是空的。</span><span class="sxs-lookup"><span data-stu-id="a418a-156">If this value is unknown, the property is empty.</span></span>

</dd> <dt>

<span data-ttu-id="a418a-157">**InstalledOn**</span><span class="sxs-lookup"><span data-stu-id="a418a-157">**InstalledOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a418a-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a418a-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a418a-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a418a-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a418a-160">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SOFTWARE \\ \\ Microsoft \\ \\ Windows NT CurrentVersion 的修正 \\ \\ \\ \\ 程式" ) </span><span class="sxs-lookup"><span data-stu-id="a418a-160">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="a418a-161">安裝更新的日期。</span><span class="sxs-lookup"><span data-stu-id="a418a-161">Date that the update was installed.</span></span> <span data-ttu-id="a418a-162">如果這個值是未知的，則屬性是空的。</span><span class="sxs-lookup"><span data-stu-id="a418a-162">If this value is unknown, the property is empty.</span></span>

> [!Note]  
> <span data-ttu-id="a418a-163">根據 QuickFix 的安裝時間，此屬性可能會使用不同的格式。</span><span class="sxs-lookup"><span data-stu-id="a418a-163">This property may use different formats, depending on when the QuickFix was installed.</span></span> <span data-ttu-id="a418a-164">大部分的系統都會使用標準日期格式，例如 "23-10-2013"。</span><span class="sxs-lookup"><span data-stu-id="a418a-164">Most systems use a standard date format, such as "23-10-2013".</span></span> <span data-ttu-id="a418a-165">不過，某些系統可能會以 Win32 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) 格式傳回64位的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="a418a-165">However, some systems may return a 64-bit hexidecimal value in the Win32 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) format.</span></span>

 

</dd> <dt>

<span data-ttu-id="a418a-166">**名稱**</span><span class="sxs-lookup"><span data-stu-id="a418a-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a418a-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a418a-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a418a-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a418a-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a418a-169">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="a418a-169">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a418a-170">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="a418a-170">Label by which the object is known.</span></span> <span data-ttu-id="a418a-171">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="a418a-171">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a418a-172">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a418a-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a418a-173">**ServicePackInEffect**</span><span class="sxs-lookup"><span data-stu-id="a418a-173">**ServicePackInEffect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a418a-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a418a-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a418a-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a418a-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a418a-176">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (260) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SOFTWARE \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ " ) </span><span class="sxs-lookup"><span data-stu-id="a418a-176">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="a418a-177">套用更新時，Service pack 會生效。</span><span class="sxs-lookup"><span data-stu-id="a418a-177">Service pack in effect when the update was applied.</span></span> <span data-ttu-id="a418a-178">如果未套用 service pack，屬性會接受值 SP0。</span><span class="sxs-lookup"><span data-stu-id="a418a-178">If no service pack has been applied, the property takes on the value SP0.</span></span> <span data-ttu-id="a418a-179">如果無法判斷哪一個 service pack 作用中，則此屬性為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a418a-179">If it cannot be determined what service pack was in effect, this property is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a418a-180">**狀態**</span><span class="sxs-lookup"><span data-stu-id="a418a-180">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a418a-181">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a418a-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a418a-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a418a-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a418a-183">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="a418a-183">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a418a-184">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="a418a-184">String that indicates the current status of the object.</span></span> <span data-ttu-id="a418a-185">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="a418a-185">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a418a-186">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="a418a-186">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a418a-187">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="a418a-187">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a418a-188">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="a418a-188">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a418a-189">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="a418a-189">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a418a-190">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="a418a-190">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a418a-191">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a418a-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a418a-192">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="a418a-192">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a418a-193">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="a418a-193">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a418a-194">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="a418a-194">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a418a-195">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="a418a-195">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a418a-196">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="a418a-196">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a418a-197">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="a418a-197">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a418a-198">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="a418a-198">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a418a-199">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="a418a-199">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a418a-200">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="a418a-200">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a418a-201">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="a418a-201">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a418a-202">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="a418a-202">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a418a-203">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="a418a-203">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a418a-204">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="a418a-204">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="a418a-205"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a418a-205"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="a418a-206">備註</span><span class="sxs-lookup"><span data-stu-id="a418a-206">Remarks</span></span>

<span data-ttu-id="a418a-207">**Win32 \_ QuickFixEngineering** 類別衍生自 [**CIM \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a418a-207">The **Win32\_QuickFixEngineering** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="a418a-208">因為更新會儲存在兩個位置中，所以這個類別的列舉可能會產生重複的專案。</span><span class="sxs-lookup"><span data-stu-id="a418a-208">Because updates are stored in two places, an enumeration of this class can result in duplicates.</span></span>

<span data-ttu-id="a418a-209">熱修正是 Microsoft 快速修正工程團隊所產生的暫時性作業系統修補程式。</span><span class="sxs-lookup"><span data-stu-id="a418a-209">A hot fix is a temporary operating system patch produced by the Quick Fix Engineering group at Microsoft.</span></span> <span data-ttu-id="a418a-210">如同 service pack，熱修正代表在作業系統發行之後，對 Windows 版本所做的變更。</span><span class="sxs-lookup"><span data-stu-id="a418a-210">Like service packs, hot fixes represent changes that have been made to a version of Windows after the operating system has been released.</span></span>

<span data-ttu-id="a418a-211">不像 service pack，熱修正並非適用于所有電腦上的完整安裝。</span><span class="sxs-lookup"><span data-stu-id="a418a-211">Unlike service packs, hot fixes are not intended for blanket installation on all computers.</span></span> <span data-ttu-id="a418a-212">相反地，它們是為了解決特定電腦設定而開發的特定問題。</span><span class="sxs-lookup"><span data-stu-id="a418a-212">Instead, they are developed to address very specific problems, often for specific computer configurations.</span></span>

<span data-ttu-id="a418a-213">此外，熱修正代表不相依于其他已釋放熱修正的獨立安裝。</span><span class="sxs-lookup"><span data-stu-id="a418a-213">In addition, hot fixes represent independent installations that do not depend on other released hot fixes.</span></span> <span data-ttu-id="a418a-214">例如，假設性熱修正4不包含熱修正1、2和3中包含的錯誤修正和功能。</span><span class="sxs-lookup"><span data-stu-id="a418a-214">For example, a hypothetical hot fix 4 would not include the bug fixes and functionality included in hot fixes 1, 2, and 3.</span></span> <span data-ttu-id="a418a-215">在大多數情況下，您也不需要先安裝熱修正1、2和3，再安裝熱修正程式4。</span><span class="sxs-lookup"><span data-stu-id="a418a-215">In most cases, there would also be no requirement that you install hot fixes 1, 2, and 3 before installing hot fix 4.</span></span> <span data-ttu-id="a418a-216">這讓個別熱修正的列舉成為重要的系統管理工作：若要知道電腦的確切設定，您不僅需要知道已安裝的 service pack，還需要知道已安裝的個別熱修正。</span><span class="sxs-lookup"><span data-stu-id="a418a-216">This makes enumeration of individual hot fixes an important administrative task: to know the exact configuration of a computer, you need to know not only which service packs have been installed but also which individual hot fixes have been installed.</span></span>

<span data-ttu-id="a418a-217">**Win32 \_ QuickFixEngineering** 類別可讓您列舉電腦上已安裝的所有熱修正程式</span><span class="sxs-lookup"><span data-stu-id="a418a-217">The **Win32\_QuickFixEngineering** class enables you to enumerate all the hot fixes that have been installed on a computer</span></span>

## <a name="examples"></a><span data-ttu-id="a418a-218">範例</span><span class="sxs-lookup"><span data-stu-id="a418a-218">Examples</span></span>

<span data-ttu-id="a418a-219">[ [取得已安裝的程式](https://Gallery.TechNet.Microsoft.Com/Get-Installed-Programs-fae091ed) ] PowerShell 範例會傳回已安裝程式的完整清單。</span><span class="sxs-lookup"><span data-stu-id="a418a-219">The [Get Installed Programs](https://Gallery.TechNet.Microsoft.Com/Get-Installed-Programs-fae091ed) PowerShell example returns a full list of installed programs.</span></span>

<span data-ttu-id="a418a-220">下列 VBScript 範例會列舉電腦上已安裝的熱修正</span><span class="sxs-lookup"><span data-stu-id="a418a-220">The following VBScript sample enumerates the installed hot fixes on a computer</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colQuickFixes = objWMIService.ExecQuery("SELECT * FROM Win32_QuickFixEngineering")
For Each objQuickFix in colQuickFixes
 Wscript.Echo "Computer: " & objQuickFix.CSName
 Wscript.Echo "Description: " & objQuickFix.Description
 Wscript.Echo "Hot Fix ID: " & objQuickFix.HotFixID
 Wscript.Echo "Installation Date: " & objQuickFix.InstallDate
 Wscript.Echo "Installed By: " & objQuickFix.InstalledBy
Next
```



## <a name="requirements"></a><span data-ttu-id="a418a-221">規格需求</span><span class="sxs-lookup"><span data-stu-id="a418a-221">Requirements</span></span>



| <span data-ttu-id="a418a-222">需求</span><span class="sxs-lookup"><span data-stu-id="a418a-222">Requirement</span></span> | <span data-ttu-id="a418a-223">值</span><span class="sxs-lookup"><span data-stu-id="a418a-223">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a418a-224">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a418a-224">Minimum supported client</span></span><br/> | <span data-ttu-id="a418a-225">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a418a-225">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a418a-226">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a418a-226">Minimum supported server</span></span><br/> | <span data-ttu-id="a418a-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a418a-227">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a418a-228">命名空間</span><span class="sxs-lookup"><span data-stu-id="a418a-228">Namespace</span></span><br/>                | <span data-ttu-id="a418a-229">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a418a-229">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a418a-230">MOF</span><span class="sxs-lookup"><span data-stu-id="a418a-230">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a418a-231"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a418a-231"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a418a-232">DLL</span><span class="sxs-lookup"><span data-stu-id="a418a-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a418a-233"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a418a-233"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a418a-234">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a418a-234">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a418a-235">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="a418a-235">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="a418a-236">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="a418a-236">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="a418a-237">WMI 工作：作業系統</span><span class="sxs-lookup"><span data-stu-id="a418a-237">WMI Tasks: Operating Systems</span></span>](../wmisdk/wmi-tasks--operating-systems.md)
</dt> </dl>

 

 
