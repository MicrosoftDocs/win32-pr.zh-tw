---
description: Win32 \_ ComClassEmulator 關聯 WMI 類別會將元件物件模型的兩個版本關聯 (COM) 類別。
ms.assetid: 33899c1e-911d-49ad-be25-355dcdb8f0c7
ms.tgt_platform: multiple
title: Win32_ComClassEmulator 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComClassEmulator
- Win32_ComClassEmulator.NewVersion
- Win32_ComClassEmulator.OldVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9966ed85b0e0b4eeb25073e13ad679759f1d460b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110240"
---
# <a name="win32_comclassemulator-class"></a><span data-ttu-id="c0fc4-103">Win32 \_ ComClassEmulator 類別</span><span class="sxs-lookup"><span data-stu-id="c0fc4-103">Win32\_ComClassEmulator class</span></span>

<span data-ttu-id="c0fc4-104">**Win32 \_ ComClassEmulator** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會將元件物件模型的兩個版本關聯 (COM) 類別。</span><span class="sxs-lookup"><span data-stu-id="c0fc4-104">The **Win32\_ComClassEmulator** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates two versions of a Component Object Model (COM) class.</span></span>

<span data-ttu-id="c0fc4-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c0fc4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c0fc4-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="c0fc4-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0fc4-107">語法</span><span class="sxs-lookup"><span data-stu-id="c0fc4-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5C-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComClassEmulator
{
  Win32_ClassicCOMClass REF NewVersion;
  Win32_ClassicCOMClass REF OldVersion;
};
```

## <a name="members"></a><span data-ttu-id="c0fc4-108">成員</span><span class="sxs-lookup"><span data-stu-id="c0fc4-108">Members</span></span>

<span data-ttu-id="c0fc4-109">**Win32 \_ ComClassEmulator** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c0fc4-109">The **Win32\_ComClassEmulator** class has these types of members:</span></span>

-   [<span data-ttu-id="c0fc4-110">屬性</span><span class="sxs-lookup"><span data-stu-id="c0fc4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0fc4-111">屬性</span><span class="sxs-lookup"><span data-stu-id="c0fc4-111">Properties</span></span>

<span data-ttu-id="c0fc4-112">**Win32 \_ ComClassEmulator** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c0fc4-112">The **Win32\_ComClassEmulator** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c0fc4-113">**NewVersion**</span><span class="sxs-lookup"><span data-stu-id="c0fc4-113">**NewVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0fc4-114">資料類型： **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="c0fc4-114">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="c0fc4-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0fc4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0fc4-116">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ ClassicCOMClass" ) </span><span class="sxs-lookup"><span data-stu-id="c0fc4-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="c0fc4-117">代表 COM 元件的實例的參考，該元件包含模擬舊版元件的介面。</span><span class="sxs-lookup"><span data-stu-id="c0fc4-117">Reference to the instance representing the COM component that contains interfaces emulating the older version of the component.</span></span>

</dd> <dt>

<span data-ttu-id="c0fc4-118">**OldVersion**</span><span class="sxs-lookup"><span data-stu-id="c0fc4-118">**OldVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0fc4-119">資料類型： **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="c0fc4-119">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="c0fc4-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0fc4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0fc4-121">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ ClassicCOMClass" ) </span><span class="sxs-lookup"><span data-stu-id="c0fc4-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="c0fc4-122">代表 COM 元件之實例的參考，該元件具有可由新版本的元件模擬的介面。</span><span class="sxs-lookup"><span data-stu-id="c0fc4-122">Reference to the instance representing the COM component with interfaces that can be emulated by the new version of the component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0fc4-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0fc4-123">Requirements</span></span>



| <span data-ttu-id="c0fc4-124">需求</span><span class="sxs-lookup"><span data-stu-id="c0fc4-124">Requirement</span></span> | <span data-ttu-id="c0fc4-125">值</span><span class="sxs-lookup"><span data-stu-id="c0fc4-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0fc4-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0fc4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c0fc4-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0fc4-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c0fc4-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0fc4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c0fc4-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0fc4-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c0fc4-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="c0fc4-130">Namespace</span></span><br/>                | <span data-ttu-id="c0fc4-131">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c0fc4-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c0fc4-132">MOF</span><span class="sxs-lookup"><span data-stu-id="c0fc4-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0fc4-133"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0fc4-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0fc4-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c0fc4-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0fc4-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0fc4-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0fc4-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0fc4-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="c0fc4-137">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c0fc4-137">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

