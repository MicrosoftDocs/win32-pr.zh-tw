---
title: DXCoreHardwareID
description: 代表介面卡的 PnP 硬體識別碼部分。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6882d9aa16bf72fb33f9a254a6434becb37f9cb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092797"
---
# <a name="dxcorehardwareid-structure"></a><span data-ttu-id="da5f7-103">DXCoreHardwareID 結構</span><span class="sxs-lookup"><span data-stu-id="da5f7-103">DXCoreHardwareID structure</span></span>

<span data-ttu-id="da5f7-104">代表介面卡的 PnP 硬體識別碼部分。</span><span class="sxs-lookup"><span data-stu-id="da5f7-104">Represents the PnP hardware ID parts for an adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="da5f7-105">語法</span><span class="sxs-lookup"><span data-stu-id="da5f7-105">Syntax</span></span>

```cpp
struct DXCoreHardwareID
{
  uint32_t vendorID;
  uint32_t deviceID;
  uint32_t subSysID;
  uint32_t revision;
};
```

## <a name="members"></a><span data-ttu-id="da5f7-106">成員</span><span class="sxs-lookup"><span data-stu-id="da5f7-106">Members</span></span>

### <a name="vendorid"></a><span data-ttu-id="da5f7-107">vendorId</span><span class="sxs-lookup"><span data-stu-id="da5f7-107">vendorId</span></span>

<span data-ttu-id="da5f7-108">類型： **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="da5f7-108">Type: **uint32_t\***</span></span>

<span data-ttu-id="da5f7-109">介面卡硬體廠商的 PCI 識別碼。</span><span class="sxs-lookup"><span data-stu-id="da5f7-109">The PCI ID of the adapter's hardware vendor.</span></span>

### <a name="deviceid"></a><span data-ttu-id="da5f7-110">deviceId</span><span class="sxs-lookup"><span data-stu-id="da5f7-110">deviceId</span></span>

<span data-ttu-id="da5f7-111">類型： **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="da5f7-111">Type: **uint32_t\***</span></span>

<span data-ttu-id="da5f7-112">介面卡硬體裝置的 PCI 識別碼。</span><span class="sxs-lookup"><span data-stu-id="da5f7-112">The PCI ID of the adapter's hardware device.</span></span>

### <a name="subsysid"></a><span data-ttu-id="da5f7-113">subSysId</span><span class="sxs-lookup"><span data-stu-id="da5f7-113">subSysId</span></span>

<span data-ttu-id="da5f7-114">類型： **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="da5f7-114">Type: **uint32_t\***</span></span>

<span data-ttu-id="da5f7-115">介面卡硬體子系統的 PCI 識別碼。</span><span class="sxs-lookup"><span data-stu-id="da5f7-115">The PCI ID of the adapter's hardware subsystem.</span></span>

### <a name="revision"></a><span data-ttu-id="da5f7-116">revision</span><span class="sxs-lookup"><span data-stu-id="da5f7-116">revision</span></span>

<span data-ttu-id="da5f7-117">類型： **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="da5f7-117">Type: **uint32_t\***</span></span>

<span data-ttu-id="da5f7-118">介面卡修訂編號的 PCI 識別碼。</span><span class="sxs-lookup"><span data-stu-id="da5f7-118">The PCI ID of the adapter's revision number.</span></span>

## <a name="see-also"></a><span data-ttu-id="da5f7-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da5f7-119">See also</span></span>

<span data-ttu-id="da5f7-120">[DXCore 參考](../dxcore-reference.md)， [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="da5f7-120">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>