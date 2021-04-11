---
description: 包含監視器的連線類型。
ms.assetid: f5658246-fbb8-4530-8dfb-f1ca792fe9d5
title: WmiMonitorConnectionParams 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorConnectionParams
- WmiMonitorConnectionParams.Active
- WmiMonitorConnectionParams.InstanceName
- WmiMonitorConnectionParams.VideoOutputTechnology
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 64212c523459696ced37e42689f6a4be0edb056b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193649"
---
# <a name="wmimonitorconnectionparams-class"></a><span data-ttu-id="1bea9-103">WmiMonitorConnectionParams 類別</span><span class="sxs-lookup"><span data-stu-id="1bea9-103">WmiMonitorConnectionParams class</span></span>

<span data-ttu-id="1bea9-104">WmiMonitorConnectionParams WMI 類別包含監視器的連線類型。</span><span class="sxs-lookup"><span data-stu-id="1bea9-104">The WmiMonitorConnectionParams WMI class contains the connection type of the monitor.</span></span>

<span data-ttu-id="1bea9-105">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1bea9-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bea9-106">語法</span><span class="sxs-lookup"><span data-stu-id="1bea9-106">Syntax</span></span>

``` syntax
class WmiMonitorConnectionParams
{
  boolean Active;
  string  InstanceName;
  uint32  VideoOutputTechnology;
};
```

## <a name="members"></a><span data-ttu-id="1bea9-107">成員</span><span class="sxs-lookup"><span data-stu-id="1bea9-107">Members</span></span>

<span data-ttu-id="1bea9-108">**WmiMonitorConnectionParams** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1bea9-108">The **WmiMonitorConnectionParams** class has these types of members:</span></span>

-   [<span data-ttu-id="1bea9-109">屬性</span><span class="sxs-lookup"><span data-stu-id="1bea9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1bea9-110">屬性</span><span class="sxs-lookup"><span data-stu-id="1bea9-110">Properties</span></span>

<span data-ttu-id="1bea9-111">**WmiMonitorConnectionParams** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1bea9-111">The **WmiMonitorConnectionParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1bea9-112">**使用中**</span><span class="sxs-lookup"><span data-stu-id="1bea9-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bea9-113">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1bea9-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1bea9-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bea9-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bea9-115">表示使用中的監視器。</span><span class="sxs-lookup"><span data-stu-id="1bea9-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="1bea9-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="1bea9-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bea9-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1bea9-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bea9-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bea9-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1bea9-119">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="1bea9-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1bea9-120">特定監視實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="1bea9-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="1bea9-121">**VideoOutputTechnology**</span><span class="sxs-lookup"><span data-stu-id="1bea9-121">**VideoOutputTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bea9-122">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1bea9-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1bea9-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bea9-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bea9-124">影片輸出技術連線類型。</span><span class="sxs-lookup"><span data-stu-id="1bea9-124">Video output technology connection type.</span></span> <span data-ttu-id="1bea9-125">有效的值記載于 [D3DKMDT \_ VIDEO \_ 輸出 \_ 技術](https://msdn.microsoft.com/library/ms794498.aspx) 列舉中。</span><span class="sxs-lookup"><span data-stu-id="1bea9-125">Valid values are documented in the [D3DKMDT\_VIDEO\_OUTPUT\_TECHNOLOGY](https://msdn.microsoft.com/library/ms794498.aspx) enumeration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1bea9-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="1bea9-126">Requirements</span></span>



| <span data-ttu-id="1bea9-127">需求</span><span class="sxs-lookup"><span data-stu-id="1bea9-127">Requirement</span></span> | <span data-ttu-id="1bea9-128">值</span><span class="sxs-lookup"><span data-stu-id="1bea9-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bea9-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1bea9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1bea9-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1bea9-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1bea9-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1bea9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1bea9-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1bea9-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1bea9-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="1bea9-133">Namespace</span></span><br/>                | <span data-ttu-id="1bea9-134">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="1bea9-134">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="1bea9-135">MOF</span><span class="sxs-lookup"><span data-stu-id="1bea9-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1bea9-136"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="1bea9-136"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="1bea9-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1bea9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bea9-138"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bea9-138"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bea9-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1bea9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bea9-140">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="1bea9-140">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




