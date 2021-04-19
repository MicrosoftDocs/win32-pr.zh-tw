---
description: 用來在埠上將 VFP 設定為強制性。
ms.assetid: efc54e06-26ff-4773-b4b4-a1c5e03d06cc
title: Msvm_EthernetSwitchPortVfpSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortVfpSettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 95d143b8e5cbc4845cc25361204fafa9efa45459
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992210"
---
# <a name="msvm_ethernetswitchportvfpsettingdata-class"></a><span data-ttu-id="c9b4a-103">Msvm \_ EthernetSwitchPortVfpSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="c9b4a-103">Msvm\_EthernetSwitchPortVfpSettingData class</span></span>

<span data-ttu-id="c9b4a-104">用來在埠上將 VFP 設定為強制性。</span><span class="sxs-lookup"><span data-stu-id="c9b4a-104">Use to set VFP as mandatory on a port.</span></span>

<span data-ttu-id="c9b4a-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c9b4a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9b4a-106">語法</span><span class="sxs-lookup"><span data-stu-id="c9b4a-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("0CB580D8-77CD-4471-956D-90ED2636FF68"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("E9B59CFA-2BE1-4B21-828F-B6FBDBDDC017"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port VFP Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortVfpSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
};
```

## <a name="members"></a><span data-ttu-id="c9b4a-107">成員</span><span class="sxs-lookup"><span data-stu-id="c9b4a-107">Members</span></span>

<span data-ttu-id="c9b4a-108">**Msvm \_ EthernetSwitchPortVfpSettingData** 類別未定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="c9b4a-108">The **Msvm\_EthernetSwitchPortVfpSettingData** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9b4a-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9b4a-109">Requirements</span></span>



| <span data-ttu-id="c9b4a-110">需求</span><span class="sxs-lookup"><span data-stu-id="c9b4a-110">Requirement</span></span> | <span data-ttu-id="c9b4a-111">值</span><span class="sxs-lookup"><span data-stu-id="c9b4a-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9b4a-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9b4a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c9b4a-113">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9b4a-113">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c9b4a-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9b4a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c9b4a-115">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c9b4a-115">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c9b4a-116">命名空間</span><span class="sxs-lookup"><span data-stu-id="c9b4a-116">Namespace</span></span><br/>                | <span data-ttu-id="c9b4a-117">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="c9b4a-117">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c9b4a-118">MOF</span><span class="sxs-lookup"><span data-stu-id="c9b4a-118">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9b4a-119"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c9b4a-119"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9b4a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c9b4a-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9b4a-121"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c9b4a-121"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c9b4a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9b4a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9b4a-123">**Msvm \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="c9b4a-123">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

 




