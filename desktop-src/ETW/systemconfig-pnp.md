---
description: 這個類別是 PnP 事件的事件型別類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 01e9a8bb-3f54-4e20-b4db-1b4bba745d4f
title: SystemConfig_PnP 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_PnP
- SystemConfig_PnP.IDLength
- SystemConfig_PnP.DescriptionLength
- SystemConfig_PnP.FriendlyNameLength
- SystemConfig_PnP.DeviceID
- SystemConfig_PnP.DeviceDescription
- SystemConfig_PnP.FriendlyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2bd4cdbbec5c61f453a0ef6fae3fef0bd494edac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468920"
---
# <a name="systemconfig_pnp-class"></a><span data-ttu-id="ce556-104">SystemConfig \_ PnP 類別</span><span class="sxs-lookup"><span data-stu-id="ce556-104">SystemConfig\_PnP class</span></span>

<span data-ttu-id="ce556-105">這個類別是 PnP 事件的事件型別類別。</span><span class="sxs-lookup"><span data-stu-id="ce556-105">This class is the event type class for PnP events.</span></span>

<span data-ttu-id="ce556-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="ce556-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce556-107">語法</span><span class="sxs-lookup"><span data-stu-id="ce556-107">Syntax</span></span>

``` syntax
[EventType(22), EventTypeName("PnP")]
class SystemConfig_PnP : SystemConfig
{
  uint32 IDLength;
  uint32 DescriptionLength;
  uint32 FriendlyNameLength;
  string DeviceID;
  string DeviceDescription;
  string FriendlyName;
};
```

## <a name="members"></a><span data-ttu-id="ce556-108">成員</span><span class="sxs-lookup"><span data-stu-id="ce556-108">Members</span></span>

<span data-ttu-id="ce556-109">**SystemConfig \_ PnP** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ce556-109">The **SystemConfig\_PnP** class has these types of members:</span></span>

-   [<span data-ttu-id="ce556-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ce556-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ce556-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ce556-111">Properties</span></span>

<span data-ttu-id="ce556-112">**SystemConfig \_ PnP** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ce556-112">The **SystemConfig\_PnP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ce556-113">**DescriptionLength**</span><span class="sxs-lookup"><span data-stu-id="ce556-113">**DescriptionLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce556-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ce556-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce556-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce556-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce556-116">限定詞： WmiDataId (2) </span><span class="sxs-lookup"><span data-stu-id="ce556-116">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="ce556-117">DeviceDescription 字串的長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="ce556-117">Length, in characters, of the DeviceDescription string.</span></span>

</dd> <dt>

<span data-ttu-id="ce556-118">**DeviceDescription**</span><span class="sxs-lookup"><span data-stu-id="ce556-118">**DeviceDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce556-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ce556-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce556-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce556-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce556-121">限定詞： WmiDataId (5) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="ce556-121">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="ce556-122">PnP 裝置的描述。</span><span class="sxs-lookup"><span data-stu-id="ce556-122">Description of the PnP device.</span></span>

</dd> <dt>

<span data-ttu-id="ce556-123">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="ce556-123">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce556-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ce556-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce556-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce556-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce556-126">限定詞： WmiDataId (4) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="ce556-126">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="ce556-127">識別 PnP 裝置。</span><span class="sxs-lookup"><span data-stu-id="ce556-127">Identifies the PnP device.</span></span>

</dd> <dt>

<span data-ttu-id="ce556-128">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="ce556-128">**FriendlyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce556-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ce556-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce556-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce556-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce556-131">限定詞： WmiDataId (6) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="ce556-131">Qualifiers: WmiDataId(6), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="ce556-132">要在使用者介面中使用的 PnP 裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="ce556-132">Name of the PnP device to use in a user interface.</span></span>

</dd> <dt>

<span data-ttu-id="ce556-133">**FriendlyNameLength**</span><span class="sxs-lookup"><span data-stu-id="ce556-133">**FriendlyNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce556-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ce556-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce556-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce556-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce556-136">限定詞： WmiDataId (3) </span><span class="sxs-lookup"><span data-stu-id="ce556-136">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="ce556-137">FriendlyName 字串的長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="ce556-137">Length, in characters, of the FriendlyName string.</span></span>

</dd> <dt>

<span data-ttu-id="ce556-138">**IDLength**</span><span class="sxs-lookup"><span data-stu-id="ce556-138">**IDLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce556-139">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ce556-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce556-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce556-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce556-141">限定詞： WmiDataId (1) </span><span class="sxs-lookup"><span data-stu-id="ce556-141">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="ce556-142">DeviceID 字串的長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="ce556-142">Length, in characters, of the DeviceID string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce556-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce556-143">Requirements</span></span>



| <span data-ttu-id="ce556-144">需求</span><span class="sxs-lookup"><span data-stu-id="ce556-144">Requirement</span></span> | <span data-ttu-id="ce556-145">值</span><span class="sxs-lookup"><span data-stu-id="ce556-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ce556-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce556-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ce556-147">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce556-147">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ce556-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce556-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ce556-149">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce556-149">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ce556-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce556-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce556-151">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="ce556-151">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




