---
description: 代表綜合鍵盤裝置。
ms.assetid: 8fe9bdd5-59e8-421d-812a-08aa3c54c88f
title: Msvm_SyntheticKeyboard 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticKeyboard
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64ac153a2c20815891d8a39fd10f58562ed8d81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973225"
---
# <a name="msvm_synthetickeyboard-class"></a><span data-ttu-id="e15b1-103">Msvm \_ SyntheticKeyboard 類別</span><span class="sxs-lookup"><span data-stu-id="e15b1-103">Msvm\_SyntheticKeyboard class</span></span>

<span data-ttu-id="e15b1-104">代表綜合鍵盤裝置。</span><span class="sxs-lookup"><span data-stu-id="e15b1-104">Represents a synthetic keyboard device.</span></span>

<span data-ttu-id="e15b1-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e15b1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e15b1-106">語法</span><span class="sxs-lookup"><span data-stu-id="e15b1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticKeyboard : CIM_UserDevice
{
};
```

## <a name="members"></a><span data-ttu-id="e15b1-107">成員</span><span class="sxs-lookup"><span data-stu-id="e15b1-107">Members</span></span>

<span data-ttu-id="e15b1-108">**Msvm \_ SyntheticKeyboard** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e15b1-108">The **Msvm\_SyntheticKeyboard** class has these types of members:</span></span>

-   [<span data-ttu-id="e15b1-109">方法</span><span class="sxs-lookup"><span data-stu-id="e15b1-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e15b1-110">方法</span><span class="sxs-lookup"><span data-stu-id="e15b1-110">Methods</span></span>

<span data-ttu-id="e15b1-111">**Msvm \_ SyntheticKeyboard** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e15b1-111">The **Msvm\_SyntheticKeyboard** class has these methods.</span></span>



| <span data-ttu-id="e15b1-112">方法</span><span class="sxs-lookup"><span data-stu-id="e15b1-112">Method</span></span>                                                                  | <span data-ttu-id="e15b1-113">描述</span><span class="sxs-lookup"><span data-stu-id="e15b1-113">Description</span></span>                         |
|:------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="e15b1-114">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="e15b1-114">**RequestStateChange**</span></span>](msvm-synthetickeyboard-requeststatechange.md) | <span data-ttu-id="e15b1-115">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="e15b1-115">Requests a state change.</span></span><br/> |
| [<span data-ttu-id="e15b1-116">**重設**</span><span class="sxs-lookup"><span data-stu-id="e15b1-116">**Reset**</span></span>](msvm-synthetickeyboard-reset.md)                           | <span data-ttu-id="e15b1-117">重設裝置。</span><span class="sxs-lookup"><span data-stu-id="e15b1-117">resets the device.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="e15b1-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e15b1-118">Requirements</span></span>



| <span data-ttu-id="e15b1-119">需求</span><span class="sxs-lookup"><span data-stu-id="e15b1-119">Requirement</span></span> | <span data-ttu-id="e15b1-120">值</span><span class="sxs-lookup"><span data-stu-id="e15b1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e15b1-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e15b1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e15b1-122">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e15b1-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e15b1-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e15b1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e15b1-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e15b1-124">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e15b1-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="e15b1-125">Namespace</span></span><br/>                | <span data-ttu-id="e15b1-126">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="e15b1-126">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e15b1-127">MOF</span><span class="sxs-lookup"><span data-stu-id="e15b1-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e15b1-128"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e15b1-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e15b1-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e15b1-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e15b1-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e15b1-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e15b1-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e15b1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e15b1-132">**CIM \_ UserDevice**</span><span class="sxs-lookup"><span data-stu-id="e15b1-132">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 

 




