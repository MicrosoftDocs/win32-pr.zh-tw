---
description: 代表 Microsoft Windows Hyper-v 平臺的服務。
ms.assetid: 309EFE4C-EEA4-454C-943D-CBF99D64FE15
title: Msvm_VirtualizationComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponent
- Msvm_VirtualizationComponent.CLSID
- Msvm_VirtualizationComponent.Context
- Msvm_VirtualizationComponent.Enabled
- Msvm_VirtualizationComponent.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 19811b224a4e93e85420539248b7d010491335aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973424"
---
# <a name="msvm_virtualizationcomponent-class"></a><span data-ttu-id="2c70e-103">Msvm \_ VirtualizationComponent 類別</span><span class="sxs-lookup"><span data-stu-id="2c70e-103">Msvm\_VirtualizationComponent class</span></span>

<span data-ttu-id="2c70e-104">代表 Microsoft Windows Hyper-v 平臺的服務。</span><span class="sxs-lookup"><span data-stu-id="2c70e-104">Represents a service of the Microsoft Windows Hyper-V platform.</span></span>

<span data-ttu-id="2c70e-105">下列語法已簡化受控物件格式 (MOF) 程式碼。</span><span class="sxs-lookup"><span data-stu-id="2c70e-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c70e-106">語法</span><span class="sxs-lookup"><span data-stu-id="2c70e-106">Syntax</span></span>

``` syntax
[Abstract]
class Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
};
```

## <a name="members"></a><span data-ttu-id="2c70e-107">成員</span><span class="sxs-lookup"><span data-stu-id="2c70e-107">Members</span></span>

<span data-ttu-id="2c70e-108">**Msvm \_ VirtualizationComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2c70e-108">The **Msvm\_VirtualizationComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="2c70e-109">屬性</span><span class="sxs-lookup"><span data-stu-id="2c70e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c70e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="2c70e-110">Properties</span></span>

<span data-ttu-id="2c70e-111">**Msvm \_ VirtualizationComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2c70e-111">The **Msvm\_VirtualizationComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c70e-112">**Clsid**</span><span class="sxs-lookup"><span data-stu-id="2c70e-112">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c70e-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2c70e-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c70e-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c70e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c70e-115">**GUID** ，表示服務 COM 物件的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c70e-115">A **GUID** that represents the class identifier of the service's COM object.</span></span>

</dd> <dt>

<span data-ttu-id="2c70e-116">**內容**</span><span class="sxs-lookup"><span data-stu-id="2c70e-116">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c70e-117">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2c70e-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2c70e-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c70e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c70e-119">限定詞：**實驗** 性</span><span class="sxs-lookup"><span data-stu-id="2c70e-119">Qualifiers: **Experimental**</span></span>
</dt> </dl>

<span data-ttu-id="2c70e-120">新建立的物件將在其中執行的內容。</span><span class="sxs-lookup"><span data-stu-id="2c70e-120">The context in which the newly created object will run.</span></span> <span data-ttu-id="2c70e-121">此值會在 *dwClsCoNtext* 參數中傳遞至 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)。</span><span class="sxs-lookup"><span data-stu-id="2c70e-121">This value is passed in the *dwClsContext* parameter to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="2c70e-122">此屬性一律設定為1。</span><span class="sxs-lookup"><span data-stu-id="2c70e-122">This property is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="2c70e-123">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="2c70e-123">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c70e-124">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2c70e-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c70e-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c70e-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c70e-126">**True** 表示已啟用此實例，可用於完成用戶端要求;否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="2c70e-126">**True** is this instance is enabled and can be used to complete client requests; otherwise, **False**.</span></span> <span data-ttu-id="2c70e-127">此屬性一律設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="2c70e-127">This property is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="2c70e-128">**名稱**</span><span class="sxs-lookup"><span data-stu-id="2c70e-128">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c70e-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2c70e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c70e-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c70e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c70e-131">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="2c70e-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2c70e-132">可唯一識別服務的語言中性字元串。</span><span class="sxs-lookup"><span data-stu-id="2c70e-132">A language-neutral string that uniquely identifies the service.</span></span> <span data-ttu-id="2c70e-133">建議採用下列格式來防止命名衝突：「廠商 \| 元件 \| 版本」。</span><span class="sxs-lookup"><span data-stu-id="2c70e-133">The following format is suggested to prevent naming conflicts: "vendor\|component\|version".</span></span> <span data-ttu-id="2c70e-134">例如，此名稱代表 Microsoft 模擬網路埠元件的1.0 版：「Microsoft EmulatedNetworkPortComponent v1.0 \| 」 \| 。</span><span class="sxs-lookup"><span data-stu-id="2c70e-134">For example, this name represents version 1.0 of the Microsoft Emulated Network Port Component: "Microsoft\|EmulatedNetworkPortComponent\|V1.0".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c70e-135">備註</span><span class="sxs-lookup"><span data-stu-id="2c70e-135">Remarks</span></span>

<span data-ttu-id="2c70e-136">存取 **Msvm \_ VirtualizationComponent** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="2c70e-136">Access to the **Msvm\_VirtualizationComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2c70e-137">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="2c70e-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c70e-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c70e-138">Requirements</span></span>



| <span data-ttu-id="2c70e-139">需求</span><span class="sxs-lookup"><span data-stu-id="2c70e-139">Requirement</span></span> | <span data-ttu-id="2c70e-140">值</span><span class="sxs-lookup"><span data-stu-id="2c70e-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c70e-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c70e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2c70e-142">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c70e-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2c70e-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c70e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2c70e-144">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c70e-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2c70e-145">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="2c70e-145">End of client support</span></span><br/>    | <span data-ttu-id="2c70e-146">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2c70e-146">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="2c70e-147">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="2c70e-147">End of server support</span></span><br/>    | <span data-ttu-id="2c70e-148">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2c70e-148">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="2c70e-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="2c70e-149">Namespace</span></span><br/>                | <span data-ttu-id="2c70e-150">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="2c70e-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2c70e-151">MOF</span><span class="sxs-lookup"><span data-stu-id="2c70e-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c70e-152"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2c70e-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c70e-153">DLL</span><span class="sxs-lookup"><span data-stu-id="2c70e-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c70e-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2c70e-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

