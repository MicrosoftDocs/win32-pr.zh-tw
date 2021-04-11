---
description: Win32 \_ ProtocolBinding 關聯 WMI 類別會將系統層級的驅動程式、網路通訊協定和網路介面卡相關聯。
ms.assetid: 09b84bb2-9999-4e80-a330-88ed6b2bd5e9
ms.tgt_platform: multiple
title: Win32_ProtocolBinding 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProtocolBinding
- Win32_ProtocolBinding.Antecedent
- Win32_ProtocolBinding.Dependent
- Win32_ProtocolBinding.Device
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 91e735a599a1dda2536fe26bcd654dcdf4b119dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847078"
---
# <a name="win32_protocolbinding-class"></a><span data-ttu-id="b95a5-103">Win32 \_ ProtocolBinding 類別</span><span class="sxs-lookup"><span data-stu-id="b95a5-103">Win32\_ProtocolBinding class</span></span>

<span data-ttu-id="b95a5-104">**Win32 \_ ProtocolBinding** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將系統層級的驅動程式、網路通訊協定和網路介面卡相關聯。</span><span class="sxs-lookup"><span data-stu-id="b95a5-104">The **Win32\_ProtocolBinding** association [WMI class](../wmisdk/retrieving-a-class.md) relates a system-level driver, network protocol, and network adapter.</span></span>

<span data-ttu-id="b95a5-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b95a5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b95a5-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="b95a5-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b95a5-107">語法</span><span class="sxs-lookup"><span data-stu-id="b95a5-107">Syntax</span></span>

``` syntax
[Dynamic, Association, Provider("CIMWin32"), UUID("{8502C509-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProtocolBinding
{
  Win32_NetworkProtocol REF Antecedent;
  Win32_SystemDriver    REF Dependent;
  Win32_NetworkAdapter  REF Device;
};
```

## <a name="members"></a><span data-ttu-id="b95a5-108">成員</span><span class="sxs-lookup"><span data-stu-id="b95a5-108">Members</span></span>

<span data-ttu-id="b95a5-109">**Win32 \_ ProtocolBinding** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b95a5-109">The **Win32\_ProtocolBinding** class has these types of members:</span></span>

-   [<span data-ttu-id="b95a5-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b95a5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b95a5-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b95a5-111">Properties</span></span>

<span data-ttu-id="b95a5-112">**Win32 \_ ProtocolBinding** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b95a5-112">The **Win32\_ProtocolBinding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b95a5-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="b95a5-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b95a5-114">資料類型： **Win32 \_ NetworkProtocol**</span><span class="sxs-lookup"><span data-stu-id="b95a5-114">Data type: **Win32\_NetworkProtocol**</span></span>
</dt> <dt>

<span data-ttu-id="b95a5-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b95a5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b95a5-116">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ NetworkProtocol" ) </span><span class="sxs-lookup"><span data-stu-id="b95a5-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkProtocol")</span></span>
</dt> </dl>

<span data-ttu-id="b95a5-117">此實例的參考，代表與系統驅動程式和網路介面卡搭配使用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b95a5-117">Reference to the instance representing the protocol that is used with the system driver and on the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b95a5-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="b95a5-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b95a5-119">資料類型： **Win32 \_ >systemdriver**</span><span class="sxs-lookup"><span data-stu-id="b95a5-119">Data type: **Win32\_SystemDriver**</span></span>
</dt> <dt>

<span data-ttu-id="b95a5-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b95a5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b95a5-121">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ >systemdriver" ) </span><span class="sxs-lookup"><span data-stu-id="b95a5-121">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SystemDriver")</span></span>
</dt> </dl>

<span data-ttu-id="b95a5-122">此實例的參考，代表透過此類別的網路通訊協定使用網路介面卡的系統驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b95a5-122">Reference to the instance representing the system driver that uses the network adapter through the network protocol of this class.</span></span>

</dd> <dt>

<span data-ttu-id="b95a5-123">**裝置**</span><span class="sxs-lookup"><span data-stu-id="b95a5-123">**Device**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b95a5-124">資料類型： **Win32 \_ NetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="b95a5-124">Data type: **Win32\_NetworkAdapter**</span></span>
</dt> <dt>

<span data-ttu-id="b95a5-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b95a5-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b95a5-126">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ NetworkAdapter" ) </span><span class="sxs-lookup"><span data-stu-id="b95a5-126">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapter")</span></span>
</dt> </dl>

<span data-ttu-id="b95a5-127">電腦系統上所使用網路介面卡的屬性。</span><span class="sxs-lookup"><span data-stu-id="b95a5-127">Properties of the network adapter being used on the computer system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b95a5-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="b95a5-128">Requirements</span></span>



| <span data-ttu-id="b95a5-129">需求</span><span class="sxs-lookup"><span data-stu-id="b95a5-129">Requirement</span></span> | <span data-ttu-id="b95a5-130">值</span><span class="sxs-lookup"><span data-stu-id="b95a5-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b95a5-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b95a5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b95a5-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b95a5-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b95a5-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b95a5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b95a5-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b95a5-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b95a5-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="b95a5-135">Namespace</span></span><br/>                | <span data-ttu-id="b95a5-136">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b95a5-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b95a5-137">MOF</span><span class="sxs-lookup"><span data-stu-id="b95a5-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b95a5-138"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b95a5-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b95a5-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b95a5-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b95a5-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b95a5-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b95a5-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b95a5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b95a5-142">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="b95a5-142">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
