---
description: 描述另一個已註冊設定檔所參考的設定檔。
ms.assetid: 36FC0161-C57F-488A-9B4A-C86C6EB481D7
title: Msvm_ReferencedProfile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencedProfile
- Msvm_ReferencedProfile.Antecedent
- Msvm_ReferencedProfile.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cbe95658556be8a15bed0e7e5b5b32dda23ff21d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979177"
---
# <a name="msvm_referencedprofile-class"></a><span data-ttu-id="582d8-103">Msvm \_ ReferencedProfile 類別</span><span class="sxs-lookup"><span data-stu-id="582d8-103">Msvm\_ReferencedProfile class</span></span>

<span data-ttu-id="582d8-104">描述另一個已註冊設定檔所參考的設定檔。</span><span class="sxs-lookup"><span data-stu-id="582d8-104">Describes a profile that is referenced by another registered profile.</span></span>

<span data-ttu-id="582d8-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="582d8-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="582d8-106">語法</span><span class="sxs-lookup"><span data-stu-id="582d8-106">Syntax</span></span>

``` syntax
class Msvm_ReferencedProfile : CIM_ReferencedProfile
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="582d8-107">成員</span><span class="sxs-lookup"><span data-stu-id="582d8-107">Members</span></span>

<span data-ttu-id="582d8-108">**Msvm \_ ReferencedProfile** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="582d8-108">The **Msvm\_ReferencedProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="582d8-109">屬性</span><span class="sxs-lookup"><span data-stu-id="582d8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="582d8-110">屬性</span><span class="sxs-lookup"><span data-stu-id="582d8-110">Properties</span></span>

<span data-ttu-id="582d8-111">**Msvm \_ ReferencedProfile** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="582d8-111">The **Msvm\_ReferencedProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="582d8-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="582d8-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="582d8-113">資料類型： **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="582d8-113">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="582d8-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="582d8-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="582d8-115">**相依** 設定檔所參考的已註冊設定檔。</span><span class="sxs-lookup"><span data-stu-id="582d8-115">The registered profile that is referenced by the **Dependent** profile.</span></span>

</dd> <dt>

<span data-ttu-id="582d8-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="582d8-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="582d8-117">資料類型： **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="582d8-117">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="582d8-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="582d8-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="582d8-119">參考其他設定檔的已註冊設定檔。</span><span class="sxs-lookup"><span data-stu-id="582d8-119">A registered profile that references other profiles.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="582d8-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="582d8-120">Requirements</span></span>



| <span data-ttu-id="582d8-121">需求</span><span class="sxs-lookup"><span data-stu-id="582d8-121">Requirement</span></span> | <span data-ttu-id="582d8-122">值</span><span class="sxs-lookup"><span data-stu-id="582d8-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="582d8-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="582d8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="582d8-124">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="582d8-124">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="582d8-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="582d8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="582d8-126">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="582d8-126">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="582d8-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="582d8-127">Namespace</span></span><br/>                | <span data-ttu-id="582d8-128">根 \\ interop</span><span class="sxs-lookup"><span data-stu-id="582d8-128">Root\\interop</span></span><br/>                                                                                |
| <span data-ttu-id="582d8-129">MOF</span><span class="sxs-lookup"><span data-stu-id="582d8-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="582d8-130"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="582d8-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="582d8-131">DLL</span><span class="sxs-lookup"><span data-stu-id="582d8-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="582d8-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="582d8-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

