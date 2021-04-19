---
description: Win32 \_ AUTOCHKSETTING WMI 類別代表磁片之 autocheck 操作的設定。
ms.assetid: 637f4d5d-f2f0-4fe0-bbde-7804156979b7
ms.tgt_platform: multiple
title: Win32_AutochkSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AutochkSetting
- Win32_AutochkSetting.Caption
- Win32_AutochkSetting.Description
- Win32_AutochkSetting.SettingID
- Win32_AutochkSetting.UserInputDelay
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea3da60cd4075aa2e36285d30950d3a105d59354
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973181"
---
# <a name="win32_autochksetting-class"></a><span data-ttu-id="9dc85-103">Win32 \_ AutochkSetting 類別</span><span class="sxs-lookup"><span data-stu-id="9dc85-103">Win32\_AutochkSetting class</span></span>

<span data-ttu-id="9dc85-104">**Win32 \_ AutochkSetting** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表磁片之 autocheck 操作的設定。</span><span class="sxs-lookup"><span data-stu-id="9dc85-104">The **Win32\_AutochkSetting** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings for the autocheck operation of a disk.</span></span>

<span data-ttu-id="9dc85-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9dc85-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9dc85-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="9dc85-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dc85-107">語法</span><span class="sxs-lookup"><span data-stu-id="9dc85-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, AMENDMENT]
class Win32_AutochkSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 UserInputDelay;
};
```

## <a name="members"></a><span data-ttu-id="9dc85-108">成員</span><span class="sxs-lookup"><span data-stu-id="9dc85-108">Members</span></span>

<span data-ttu-id="9dc85-109">**Win32 \_ AutochkSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9dc85-109">The **Win32\_AutochkSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="9dc85-110">屬性</span><span class="sxs-lookup"><span data-stu-id="9dc85-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9dc85-111">屬性</span><span class="sxs-lookup"><span data-stu-id="9dc85-111">Properties</span></span>

<span data-ttu-id="9dc85-112">**Win32 \_ AutochkSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9dc85-112">The **Win32\_AutochkSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9dc85-113">**標題**</span><span class="sxs-lookup"><span data-stu-id="9dc85-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dc85-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9dc85-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dc85-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9dc85-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9dc85-116">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="9dc85-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9dc85-117">目前物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="9dc85-117">Short textual description of the current object.</span></span>

<span data-ttu-id="9dc85-118">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="9dc85-118">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="9dc85-119">**說明**</span><span class="sxs-lookup"><span data-stu-id="9dc85-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dc85-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9dc85-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dc85-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9dc85-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9dc85-122">目前物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="9dc85-122">Textual description of the current object.</span></span>

<span data-ttu-id="9dc85-123">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="9dc85-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="9dc85-124">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="9dc85-124">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dc85-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9dc85-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dc85-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9dc85-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9dc85-127">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SettingId" ) ，索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9dc85-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingId"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9dc85-128">用來作為目前物件之索引鍵一部分的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9dc85-128">An ID that is used as part of a key for the current object.</span></span>

</dd> <dt>

<span data-ttu-id="9dc85-129">**UserInputDelay**</span><span class="sxs-lookup"><span data-stu-id="9dc85-129">**UserInputDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dc85-130">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9dc85-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9dc85-131">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9dc85-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9dc85-132">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKLM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \| AutoChkTimeOut" ) ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "seconds" ) </span><span class="sxs-lookup"><span data-stu-id="9dc85-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKLM\\\\CurrentControlSet\\\\Control\\\\Session Manager \| AutoChkTimeOut"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="9dc85-133">Autocheck 的使用者輸入延遲。</span><span class="sxs-lookup"><span data-stu-id="9dc85-133">The user input delay for autocheck.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9dc85-134">備註</span><span class="sxs-lookup"><span data-stu-id="9dc85-134">Remarks</span></span>

<span data-ttu-id="9dc85-135">**Win32 \_ AutochkSetting** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="9dc85-135">The **Win32\_AutochkSetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9dc85-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="9dc85-136">Requirements</span></span>



| <span data-ttu-id="9dc85-137">需求</span><span class="sxs-lookup"><span data-stu-id="9dc85-137">Requirement</span></span> | <span data-ttu-id="9dc85-138">值</span><span class="sxs-lookup"><span data-stu-id="9dc85-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9dc85-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9dc85-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9dc85-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9dc85-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9dc85-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9dc85-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9dc85-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9dc85-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9dc85-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="9dc85-143">Namespace</span></span><br/>                | <span data-ttu-id="9dc85-144">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9dc85-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9dc85-145">MOF</span><span class="sxs-lookup"><span data-stu-id="9dc85-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9dc85-146"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="9dc85-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9dc85-147">DLL</span><span class="sxs-lookup"><span data-stu-id="9dc85-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dc85-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dc85-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dc85-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9dc85-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dc85-150">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="9dc85-150">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="9dc85-151">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="9dc85-151">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

