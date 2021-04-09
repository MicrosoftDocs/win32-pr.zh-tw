---
description: Win32 \_ ComClassAutoEmulator 關聯 WMI 類別會建立元件物件模型 (COM) 類別和它自動模擬的另一個 com 類別之間的關聯。
ms.assetid: e060ba26-98e7-47cb-bf21-1ca80d0e8a07
ms.tgt_platform: multiple
title: Win32_ComClassAutoEmulator 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComClassAutoEmulator
- Win32_ComClassAutoEmulator.NewVersion
- Win32_ComClassAutoEmulator.OldVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9442036d43859caa5fa277109c7e85553e7d42f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111229"
---
# <a name="win32_comclassautoemulator-class"></a><span data-ttu-id="e3d9d-103">Win32 \_ ComClassAutoEmulator 類別</span><span class="sxs-lookup"><span data-stu-id="e3d9d-103">Win32\_ComClassAutoEmulator class</span></span>

<span data-ttu-id="e3d9d-104">**Win32 \_ ComClassAutoEmulator** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會建立元件物件模型 (COM) 類別和它自動模擬的另一個 com 類別之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="e3d9d-104">The **Win32\_ComClassAutoEmulator** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a Component Object Model (COM) class and another COM class that it automatically emulates.</span></span>

<span data-ttu-id="e3d9d-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e3d9d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e3d9d-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="e3d9d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3d9d-107">語法</span><span class="sxs-lookup"><span data-stu-id="e3d9d-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5D-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComClassAutoEmulator
{
  Win32_ClassicCOMClass REF NewVersion;
  Win32_ClassicCOMClass REF OldVersion;
};
```

## <a name="members"></a><span data-ttu-id="e3d9d-108">成員</span><span class="sxs-lookup"><span data-stu-id="e3d9d-108">Members</span></span>

<span data-ttu-id="e3d9d-109">**Win32 \_ ComClassAutoEmulator** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e3d9d-109">The **Win32\_ComClassAutoEmulator** class has these types of members:</span></span>

-   [<span data-ttu-id="e3d9d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="e3d9d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e3d9d-111">屬性</span><span class="sxs-lookup"><span data-stu-id="e3d9d-111">Properties</span></span>

<span data-ttu-id="e3d9d-112">**Win32 \_ ComClassAutoEmulator** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e3d9d-112">The **Win32\_ComClassAutoEmulator** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e3d9d-113">**NewVersion**</span><span class="sxs-lookup"><span data-stu-id="e3d9d-113">**NewVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d9d-114">資料類型： **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="e3d9d-114">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="e3d9d-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e3d9d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3d9d-116">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ ClassicCOMClass" ) </span><span class="sxs-lookup"><span data-stu-id="e3d9d-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="e3d9d-117">代表可自動模擬相關聯 COM 元件之 COM 元件的實例參考。</span><span class="sxs-lookup"><span data-stu-id="e3d9d-117">Reference to the instance representing the COM component that can automatically emulate the associated COM component.</span></span> <span data-ttu-id="e3d9d-118">這項資訊是透過 AutoTreatAs 登錄專案取得。</span><span class="sxs-lookup"><span data-stu-id="e3d9d-118">This information is obtained through the AutoTreatAs registry entry.</span></span>

</dd> <dt>

<span data-ttu-id="e3d9d-119">**OldVersion**</span><span class="sxs-lookup"><span data-stu-id="e3d9d-119">**OldVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3d9d-120">資料類型： **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="e3d9d-120">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="e3d9d-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e3d9d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3d9d-122">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ ClassicCOMClass" ) </span><span class="sxs-lookup"><span data-stu-id="e3d9d-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="e3d9d-123">實例的參考，代表由另一個元件自動模擬的 COM 元件。</span><span class="sxs-lookup"><span data-stu-id="e3d9d-123">Reference to the instance representing the COM component that is automatically emulated by another component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e3d9d-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3d9d-124">Requirements</span></span>



| <span data-ttu-id="e3d9d-125">需求</span><span class="sxs-lookup"><span data-stu-id="e3d9d-125">Requirement</span></span> | <span data-ttu-id="e3d9d-126">值</span><span class="sxs-lookup"><span data-stu-id="e3d9d-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3d9d-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e3d9d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e3d9d-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3d9d-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e3d9d-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e3d9d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e3d9d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3d9d-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e3d9d-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="e3d9d-131">Namespace</span></span><br/>                | <span data-ttu-id="e3d9d-132">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e3d9d-132">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e3d9d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="e3d9d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3d9d-134"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3d9d-134"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3d9d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e3d9d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3d9d-136"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3d9d-136"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3d9d-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3d9d-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="e3d9d-138">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e3d9d-138">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

