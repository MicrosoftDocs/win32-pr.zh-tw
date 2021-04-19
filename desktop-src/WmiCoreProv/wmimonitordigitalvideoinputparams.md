---
description: 代表數位視訊的輸入參數。
ms.assetid: aa459612-db79-477b-891f-28c9d0b1b497
title: WmiMonitorDigitalVideoInputParams 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDigitalVideoInputParams
- WmiMonitorDigitalVideoInputParams.Active
- WmiMonitorDigitalVideoInputParams.InstanceName
- WmiMonitorDigitalVideoInputParams.IsDFP1xCompatible
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: a08e38a38bb5f5e8d539fabdf69c429c42f4b1f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975817"
---
# <a name="wmimonitordigitalvideoinputparams-class"></a><span data-ttu-id="ed17a-103">WmiMonitorDigitalVideoInputParams 類別</span><span class="sxs-lookup"><span data-stu-id="ed17a-103">WmiMonitorDigitalVideoInputParams class</span></span>

<span data-ttu-id="ed17a-104">**WmiMonitorDigitalVideoInputParams** 代表數位視訊的輸入參數。</span><span class="sxs-lookup"><span data-stu-id="ed17a-104">The **WmiMonitorDigitalVideoInputParams** represents input parameters for digital video.</span></span> <span data-ttu-id="ed17a-105">此類別中的資料會對應至視頻電子郵件標準關聯的影片輸入定義中的資料 (VESA) 增強的擴充顯示器識別資料 (E-EDID) 標準。</span><span class="sxs-lookup"><span data-stu-id="ed17a-105">The data in this class corresponds to data in the Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span> <span data-ttu-id="ed17a-106">只有當 [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md)類別的 **VideoInputType** 屬性值為 "數位" 時，才能使用這個類別的實例。</span><span class="sxs-lookup"><span data-stu-id="ed17a-106">An instance of this class is available only when the value of the **VideoInputType** property of the [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) class is "Digital".</span></span>

## <a name="syntax"></a><span data-ttu-id="ed17a-107">語法</span><span class="sxs-lookup"><span data-stu-id="ed17a-107">Syntax</span></span>

``` syntax
class WmiMonitorDigitalVideoInputParams : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  boolean IsDFP1xCompatible;
};
```

## <a name="members"></a><span data-ttu-id="ed17a-108">成員</span><span class="sxs-lookup"><span data-stu-id="ed17a-108">Members</span></span>

<span data-ttu-id="ed17a-109">**WmiMonitorDigitalVideoInputParams** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ed17a-109">The **WmiMonitorDigitalVideoInputParams** class has these types of members:</span></span>

-   [<span data-ttu-id="ed17a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ed17a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ed17a-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ed17a-111">Properties</span></span>

<span data-ttu-id="ed17a-112">**WmiMonitorDigitalVideoInputParams** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ed17a-112">The **WmiMonitorDigitalVideoInputParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ed17a-113">**使用中**</span><span class="sxs-lookup"><span data-stu-id="ed17a-113">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed17a-114">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ed17a-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ed17a-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ed17a-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed17a-116">表示使用中的監視器。</span><span class="sxs-lookup"><span data-stu-id="ed17a-116">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="ed17a-117">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="ed17a-117">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed17a-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ed17a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed17a-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ed17a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed17a-120">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="ed17a-120">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ed17a-121">特定監視實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed17a-121">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="ed17a-122">**IsDFP1xCompatible**</span><span class="sxs-lookup"><span data-stu-id="ed17a-122">**IsDFP1xCompatible**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed17a-123">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ed17a-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ed17a-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ed17a-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed17a-125">VESA DFP 1.x 或相容。</span><span class="sxs-lookup"><span data-stu-id="ed17a-125">VESA DFP 1.x or compatible.</span></span> <span data-ttu-id="ed17a-126">如果設定，介面與 VESA 數位平面面板的信號相容 (DFP) 1.x 轉換最小化差異信號 (TMDS) CRGB、1圖元/時鐘、最多8個位/色彩最高 (MSB) 對齊、DE 高。</span><span class="sxs-lookup"><span data-stu-id="ed17a-126">If set, interface is signal compatible with VESA Digital Flat Panel (DFP) 1.x Transition Minimized Differential Signaling (TMDS) CRGB, 1 pixel/clock, up to 8 bits/color most significant bit (MSB) aligned, DE active high.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed17a-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed17a-127">Requirements</span></span>



| <span data-ttu-id="ed17a-128">需求</span><span class="sxs-lookup"><span data-stu-id="ed17a-128">Requirement</span></span> | <span data-ttu-id="ed17a-129">值</span><span class="sxs-lookup"><span data-stu-id="ed17a-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed17a-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed17a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ed17a-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed17a-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ed17a-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ed17a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ed17a-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed17a-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ed17a-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="ed17a-134">Namespace</span></span><br/>                | <span data-ttu-id="ed17a-135">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="ed17a-135">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="ed17a-136">MOF</span><span class="sxs-lookup"><span data-stu-id="ed17a-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed17a-137"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed17a-137"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed17a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ed17a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed17a-139"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed17a-139"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed17a-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed17a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed17a-141">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="ed17a-141">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




