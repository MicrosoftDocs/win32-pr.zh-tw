---
description: Win32 \_ COMSetting ABSTRACT WMI 類別代表與元件物件模型相關聯的設定， (com) 元件或 com 應用程式。
ms.assetid: e8cdbee8-41ab-4aff-b17b-707667138411
ms.tgt_platform: multiple
title: Win32_COMSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMSetting
- Win32_COMSetting.Caption
- Win32_COMSetting.Description
- Win32_COMSetting.SettingID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5ec7932117d1ff0bc058d2b9a131f77ff9e040bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187645"
---
# <a name="win32_comsetting-class"></a><span data-ttu-id="64980-103">Win32 \_ COMSetting 類別</span><span class="sxs-lookup"><span data-stu-id="64980-103">Win32\_COMSetting class</span></span>

<span data-ttu-id="64980-104">**Win32 \_ COMSetting** abstract [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表與元件物件模型相關聯的設定， (com) 元件或 com 應用程式。</span><span class="sxs-lookup"><span data-stu-id="64980-104">The **Win32\_COMSetting** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings associated with a Component Object Model (COM) component or COM application.</span></span>

<span data-ttu-id="64980-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="64980-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="64980-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="64980-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="64980-107">語法</span><span class="sxs-lookup"><span data-stu-id="64980-107">Syntax</span></span>

``` syntax
[abstract, UUID("{E5D8A560-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_COMSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
};
```

## <a name="members"></a><span data-ttu-id="64980-108">成員</span><span class="sxs-lookup"><span data-stu-id="64980-108">Members</span></span>

<span data-ttu-id="64980-109">**Win32 \_ COMSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="64980-109">The **Win32\_COMSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="64980-110">屬性</span><span class="sxs-lookup"><span data-stu-id="64980-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="64980-111">屬性</span><span class="sxs-lookup"><span data-stu-id="64980-111">Properties</span></span>

<span data-ttu-id="64980-112">**Win32 \_ COMSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="64980-112">The **Win32\_COMSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="64980-113">**標題**</span><span class="sxs-lookup"><span data-stu-id="64980-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64980-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="64980-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64980-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64980-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64980-116">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="64980-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="64980-117">目前物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="64980-117">Short textual description of the current object.</span></span>

<span data-ttu-id="64980-118">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="64980-118">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="64980-119">**說明**</span><span class="sxs-lookup"><span data-stu-id="64980-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64980-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="64980-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64980-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64980-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64980-122">目前物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="64980-122">Textual description of the current object.</span></span>

<span data-ttu-id="64980-123">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="64980-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="64980-124">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="64980-124">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64980-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="64980-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64980-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64980-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64980-127">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="64980-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="64980-128">已知目前物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="64980-128">Identifier by which the current object is known.</span></span>

<span data-ttu-id="64980-129">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="64980-129">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64980-130">備註</span><span class="sxs-lookup"><span data-stu-id="64980-130">Remarks</span></span>

<span data-ttu-id="64980-131">**Win32 \_ COMSetting** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="64980-131">The **Win32\_COMSetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="64980-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="64980-132">Requirements</span></span>



| <span data-ttu-id="64980-133">需求</span><span class="sxs-lookup"><span data-stu-id="64980-133">Requirement</span></span> | <span data-ttu-id="64980-134">值</span><span class="sxs-lookup"><span data-stu-id="64980-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64980-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="64980-135">Minimum supported client</span></span><br/> | <span data-ttu-id="64980-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64980-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="64980-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="64980-137">Minimum supported server</span></span><br/> | <span data-ttu-id="64980-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64980-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="64980-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="64980-139">Namespace</span></span><br/>                | <span data-ttu-id="64980-140">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="64980-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="64980-141">MOF</span><span class="sxs-lookup"><span data-stu-id="64980-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64980-142"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="64980-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="64980-143">DLL</span><span class="sxs-lookup"><span data-stu-id="64980-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64980-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64980-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64980-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64980-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64980-146">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="64980-146">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

<span data-ttu-id="64980-147">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="64980-147">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

