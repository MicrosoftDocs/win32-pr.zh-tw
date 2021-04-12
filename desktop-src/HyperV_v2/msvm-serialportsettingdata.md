---
description: 描述虛擬序列埠的設定資料。
ms.assetid: 8b257bbf-495a-4eef-86a1-70e31e4a85a5
title: Msvm_SerialPortSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortSettingData
- Msvm_SerialPortSettingData.DebuggerMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 21a1ab58608c5631a328795272d6a04aa56aedf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849488"
---
# <a name="msvm_serialportsettingdata-class"></a><span data-ttu-id="aa507-103">Msvm \_ SerialPortSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="aa507-103">Msvm\_SerialPortSettingData class</span></span>

<span data-ttu-id="aa507-104">描述虛擬序列埠的設定資料。</span><span class="sxs-lookup"><span data-stu-id="aa507-104">Describes the setting data for a virtual serial port.</span></span>

<span data-ttu-id="aa507-105">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="aa507-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa507-106">語法</span><span class="sxs-lookup"><span data-stu-id="aa507-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortSettingData : CIM_ResourceAllocationSettingData
{
  boolean DebuggerMode;
};
```

## <a name="members"></a><span data-ttu-id="aa507-107">成員</span><span class="sxs-lookup"><span data-stu-id="aa507-107">Members</span></span>

<span data-ttu-id="aa507-108">**Msvm \_ SerialPortSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="aa507-108">The **Msvm\_SerialPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="aa507-109">屬性</span><span class="sxs-lookup"><span data-stu-id="aa507-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aa507-110">屬性</span><span class="sxs-lookup"><span data-stu-id="aa507-110">Properties</span></span>

<span data-ttu-id="aa507-111">**Msvm \_ SerialPortSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="aa507-111">The **Msvm\_SerialPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aa507-112">**DebuggerMode**</span><span class="sxs-lookup"><span data-stu-id="aa507-112">**DebuggerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa507-113">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="aa507-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aa507-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aa507-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aa507-115">如果虛擬序列埠上已啟用偵錯工具模式，則為 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="aa507-115">**true** if the debugger mode is enabled on a virtual serial port; otherwise, **false**.</span></span> <span data-ttu-id="aa507-116">偵錯工具模式透過虛擬序列埠增強了 Microsoft Windows 核心偵錯工具的使用。</span><span class="sxs-lookup"><span data-stu-id="aa507-116">The debugger mode enhances the use of a Microsoft Windows kernel debugger over a virtual serial port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa507-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa507-117">Requirements</span></span>



| <span data-ttu-id="aa507-118">需求</span><span class="sxs-lookup"><span data-stu-id="aa507-118">Requirement</span></span> | <span data-ttu-id="aa507-119">值</span><span class="sxs-lookup"><span data-stu-id="aa507-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa507-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aa507-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aa507-121">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa507-121">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="aa507-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aa507-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aa507-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="aa507-123">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="aa507-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="aa507-124">Namespace</span></span><br/>                | <span data-ttu-id="aa507-125">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="aa507-125">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="aa507-126">MOF</span><span class="sxs-lookup"><span data-stu-id="aa507-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa507-127"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="aa507-127"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa507-128">DLL</span><span class="sxs-lookup"><span data-stu-id="aa507-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa507-129"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aa507-129"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="aa507-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa507-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa507-131">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="aa507-131">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




