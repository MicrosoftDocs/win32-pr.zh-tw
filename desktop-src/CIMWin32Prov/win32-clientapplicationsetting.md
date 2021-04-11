---
description: Win32 \_ ClientApplicationSetting 關聯 WMI 類別會將可執行檔和元件物件模型關聯 (com) 應用程式，其中包含可執行檔的 COM 設定選項。
ms.assetid: c43d80ee-0f29-4452-b51f-f18543bc1d35
ms.tgt_platform: multiple
title: Win32_ClientApplicationSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClientApplicationSetting
- Win32_ClientApplicationSetting.Application
- Win32_ClientApplicationSetting.Client
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fda1f1305904fa919bb2080fe5de02f0e5850a8a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936427"
---
# <a name="win32_clientapplicationsetting-class"></a><span data-ttu-id="86cd0-103">Win32 \_ ClientApplicationSetting 類別</span><span class="sxs-lookup"><span data-stu-id="86cd0-103">Win32\_ClientApplicationSetting class</span></span>

<span data-ttu-id="86cd0-104">**Win32 \_ ClientApplicationSetting** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會將可執行檔和元件物件模型關聯 (com) 應用程式，其中包含可執行檔的 COM 設定選項。</span><span class="sxs-lookup"><span data-stu-id="86cd0-104">The **Win32\_ClientApplicationSetting** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates an executable file and a Component Object Model (COM) application that contains the COM configuration options for the executable file.</span></span>

<span data-ttu-id="86cd0-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="86cd0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="86cd0-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="86cd0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="86cd0-107">語法</span><span class="sxs-lookup"><span data-stu-id="86cd0-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5E-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClientApplicationSetting
{
  Win32_DCOMApplication REF Application;
  CIM_DataFile          REF Client;
};
```

## <a name="members"></a><span data-ttu-id="86cd0-108">成員</span><span class="sxs-lookup"><span data-stu-id="86cd0-108">Members</span></span>

<span data-ttu-id="86cd0-109">**Win32 \_ ClientApplicationSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="86cd0-109">The **Win32\_ClientApplicationSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="86cd0-110">屬性</span><span class="sxs-lookup"><span data-stu-id="86cd0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="86cd0-111">屬性</span><span class="sxs-lookup"><span data-stu-id="86cd0-111">Properties</span></span>

<span data-ttu-id="86cd0-112">**Win32 \_ ClientApplicationSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="86cd0-112">The **Win32\_ClientApplicationSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="86cd0-113">**應用程式**</span><span class="sxs-lookup"><span data-stu-id="86cd0-113">**Application**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86cd0-114">資料類型： **Win32 \_ DCOMApplication**</span><span class="sxs-lookup"><span data-stu-id="86cd0-114">Data type: **Win32\_DCOMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="86cd0-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86cd0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86cd0-116">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ DCOMApplication" ) </span><span class="sxs-lookup"><span data-stu-id="86cd0-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="86cd0-117">代表 COM 應用程式之實例的參考，其中包含可執行檔的設定選項。</span><span class="sxs-lookup"><span data-stu-id="86cd0-117">Reference to the instance that represents the COM application that contains configuration options of the executable file.</span></span>

</dd> <dt>

<span data-ttu-id="86cd0-118">**用戶端**</span><span class="sxs-lookup"><span data-stu-id="86cd0-118">**Client**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86cd0-119">資料類型： **CIM 資料 \_ 檔**</span><span class="sxs-lookup"><span data-stu-id="86cd0-119">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="86cd0-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="86cd0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86cd0-121">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「cim \| cim \_ 資料檔案」 ) </span><span class="sxs-lookup"><span data-stu-id="86cd0-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_DataFile")</span></span>
</dt> </dl>

<span data-ttu-id="86cd0-122">代表使用 COM 設定之可執行檔的實例參考。</span><span class="sxs-lookup"><span data-stu-id="86cd0-122">Reference to the instance that represents the executable file that uses COM settings.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86cd0-123">備註</span><span class="sxs-lookup"><span data-stu-id="86cd0-123">Remarks</span></span>

<span data-ttu-id="86cd0-124">**Win32 \_ClientApplicationSetting** 不支援列舉。</span><span class="sxs-lookup"><span data-stu-id="86cd0-124">**Win32\_ClientApplicationSetting** does not support enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="86cd0-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="86cd0-125">Requirements</span></span>



| <span data-ttu-id="86cd0-126">需求</span><span class="sxs-lookup"><span data-stu-id="86cd0-126">Requirement</span></span> | <span data-ttu-id="86cd0-127">值</span><span class="sxs-lookup"><span data-stu-id="86cd0-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86cd0-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="86cd0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="86cd0-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86cd0-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="86cd0-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="86cd0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="86cd0-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86cd0-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="86cd0-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="86cd0-132">Namespace</span></span><br/>                | <span data-ttu-id="86cd0-133">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="86cd0-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="86cd0-134">MOF</span><span class="sxs-lookup"><span data-stu-id="86cd0-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86cd0-135"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="86cd0-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="86cd0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="86cd0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86cd0-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86cd0-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86cd0-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86cd0-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="86cd0-139">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="86cd0-139">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

