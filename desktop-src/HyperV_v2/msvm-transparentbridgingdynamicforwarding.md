---
description: 將透明橋接服務連接到動態轉寄專案， (瞭解的 MAC 位址) 。
ms.assetid: CA083F15-1E75-4EB9-BE56-95742181FDAC
title: Msvm_TransparentBridgingDynamicForwarding 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingDynamicForwarding
- Msvm_TransparentBridgingDynamicForwarding.Antecedent
- Msvm_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 01b9d9c752d4781864c07ff24fca5f866a57ae54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943682"
---
# <a name="msvm_transparentbridgingdynamicforwarding-class"></a><span data-ttu-id="81ef1-103">Msvm \_ TransparentBridgingDynamicForwarding 類別</span><span class="sxs-lookup"><span data-stu-id="81ef1-103">Msvm\_TransparentBridgingDynamicForwarding class</span></span>

<span data-ttu-id="81ef1-104">將透明橋接服務連接到動態轉寄專案， (瞭解的 MAC 位址) 。</span><span class="sxs-lookup"><span data-stu-id="81ef1-104">Connects a transparent bridging service to a dynamic forward entry (learned MAC address).</span></span>

<span data-ttu-id="81ef1-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="81ef1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="81ef1-106">語法</span><span class="sxs-lookup"><span data-stu-id="81ef1-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TransparentBridgingDynamicForwarding : CIM_TransparentBridgingDynamicForwarding
{
  Msvm_TransparentBridgingService REF Antecedent;
  Msvm_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="81ef1-107">成員</span><span class="sxs-lookup"><span data-stu-id="81ef1-107">Members</span></span>

<span data-ttu-id="81ef1-108">**Msvm \_ TransparentBridgingDynamicForwarding** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="81ef1-108">The **Msvm\_TransparentBridgingDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="81ef1-109">屬性</span><span class="sxs-lookup"><span data-stu-id="81ef1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="81ef1-110">屬性</span><span class="sxs-lookup"><span data-stu-id="81ef1-110">Properties</span></span>

<span data-ttu-id="81ef1-111">**Msvm \_ TransparentBridgingDynamicForwarding** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="81ef1-111">The **Msvm\_TransparentBridgingDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81ef1-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="81ef1-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ef1-113">資料類型： **[ **Msvm \_ TransparentBridgingService**](msvm-transparentbridgingservice.md)**</span><span class="sxs-lookup"><span data-stu-id="81ef1-113">Data type: **[**Msvm\_TransparentBridgingService**](msvm-transparentbridgingservice.md)**</span></span>
</dt> <dt>

<span data-ttu-id="81ef1-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="81ef1-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ef1-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="81ef1-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="81ef1-116">代表透明橋接服務之 [**Msvm \_ TransparentBridgingService**](msvm-transparentbridgingservice.md) 類別實例的參考。</span><span class="sxs-lookup"><span data-stu-id="81ef1-116">A reference to an instance of the [**Msvm\_TransparentBridgingService**](msvm-transparentbridgingservice.md) class that represents the transparent bridging service.</span></span>

</dd> <dt>

<span data-ttu-id="81ef1-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="81ef1-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81ef1-118">資料類型： **[ **Msvm \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span><span class="sxs-lookup"><span data-stu-id="81ef1-118">Data type: **[**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span></span>
</dt> <dt>

<span data-ttu-id="81ef1-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="81ef1-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81ef1-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="81ef1-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="81ef1-121">[**Msvm \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)類別實例的參考，該類別表示轉送資料庫的動態轉送專案。</span><span class="sxs-lookup"><span data-stu-id="81ef1-121">A reference to an instance of the [**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) class that represents the dynamic forwarding entry of the forwarding database.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81ef1-122">備註</span><span class="sxs-lookup"><span data-stu-id="81ef1-122">Remarks</span></span>

<span data-ttu-id="81ef1-123">存取 **Msvm \_ TransparentBridgingDynamicForwarding** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="81ef1-123">Access to the **Msvm\_TransparentBridgingDynamicForwarding** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="81ef1-124">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="81ef1-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="81ef1-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="81ef1-125">Requirements</span></span>



| <span data-ttu-id="81ef1-126">需求</span><span class="sxs-lookup"><span data-stu-id="81ef1-126">Requirement</span></span> | <span data-ttu-id="81ef1-127">值</span><span class="sxs-lookup"><span data-stu-id="81ef1-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81ef1-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="81ef1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="81ef1-129">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="81ef1-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="81ef1-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="81ef1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="81ef1-131">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="81ef1-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="81ef1-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="81ef1-132">Namespace</span></span><br/>                | <span data-ttu-id="81ef1-133">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="81ef1-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="81ef1-134">MOF</span><span class="sxs-lookup"><span data-stu-id="81ef1-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81ef1-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="81ef1-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="81ef1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="81ef1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81ef1-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="81ef1-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="81ef1-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81ef1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81ef1-139">**CIM \_ TransparentBridgingDynamicForwarding**</span><span class="sxs-lookup"><span data-stu-id="81ef1-139">**CIM\_TransparentBridgingDynamicForwarding**</span></span>](cim-transparentbridgingdynamicforwarding.md)
</dt> <dt>

[<span data-ttu-id="81ef1-140">**CIM \_ TransparentBridgingDynamicForwarding**</span><span class="sxs-lookup"><span data-stu-id="81ef1-140">**CIM\_TransparentBridgingDynamicForwarding**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingdynamicforwarding)
</dt> </dl>

 

