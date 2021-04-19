---
description: 埠 \_ 資訊 \_ 2 結構會識別支援的印表機埠。
ms.assetid: 93675294-61d4-40e4-b84c-f252978e0285
title: 'PORT_INFO_2 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_2
- _PORT_INFO_2A
- _PORT_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1d2186193318387bb6e37a228bd4d2fd64eca6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984592"
---
# <a name="port_info_2-structure"></a><span data-ttu-id="15ecb-103">埠 \_ 資訊 \_ 2 結構</span><span class="sxs-lookup"><span data-stu-id="15ecb-103">PORT\_INFO\_2 structure</span></span>

<span data-ttu-id="15ecb-104">**埠 \_ 資訊 \_ 2** 結構會識別支援的印表機埠。</span><span class="sxs-lookup"><span data-stu-id="15ecb-104">The **PORT\_INFO\_2** structure identifies a supported printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="15ecb-105">語法</span><span class="sxs-lookup"><span data-stu-id="15ecb-105">Syntax</span></span>


```C++
typedef struct _PORT_INFO_2 {
  LPTSTR pPortName;
  LPTSTR pMonitorName;
  LPTSTR pDescription;
  DWORD  fPortType;
  DWORD  Reserved;
} PORT_INFO_2, *PPORT_INFO_2;
```



## <a name="members"></a><span data-ttu-id="15ecb-106">成員</span><span class="sxs-lookup"><span data-stu-id="15ecb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="15ecb-107">**pPortName**</span><span class="sxs-lookup"><span data-stu-id="15ecb-107">**pPortName**</span></span>
</dt> <dd>

<span data-ttu-id="15ecb-108">識別支援之印表機埠 (以 null 終止的字串指標，例如 "LPT1：" ) 。</span><span class="sxs-lookup"><span data-stu-id="15ecb-108">Pointer to a null-terminated string that identifies a supported printer port (for example, "LPT1:").</span></span>

</dd> <dt>

<span data-ttu-id="15ecb-109">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="15ecb-109">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="15ecb-110">識別已安裝的監視器 (之以 null 結束的字串指標，例如「PJL 監視器」 ) 。</span><span class="sxs-lookup"><span data-stu-id="15ecb-110">Pointer to a null-terminated string that identifies an installed monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="15ecb-111">這可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="15ecb-111">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="15ecb-112">**pDescription**</span><span class="sxs-lookup"><span data-stu-id="15ecb-112">**pDescription**</span></span>
</dt> <dd>

<span data-ttu-id="15ecb-113">以 null 終止的字串指標，此字串會更詳細地描述埠 (例如，如果 **pPortName** 是 "LPT1："， **pDescription** 是 "printer port" ) 。</span><span class="sxs-lookup"><span data-stu-id="15ecb-113">Pointer to a null-terminated string that describes the port in more detail (for example, if **pPortName** is "LPT1:", **pDescription** is "printer port").</span></span> <span data-ttu-id="15ecb-114">這可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="15ecb-114">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="15ecb-115">**fPortType**</span><span class="sxs-lookup"><span data-stu-id="15ecb-115">**fPortType**</span></span>
</dt> <dd>

<span data-ttu-id="15ecb-116">描述埠類型的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="15ecb-116">Bitmask describing the type of port.</span></span> <span data-ttu-id="15ecb-117">這個成員可以是下列值的組合：</span><span class="sxs-lookup"><span data-stu-id="15ecb-117">This member can be a combination of the following values:</span></span>

<dl><span id="PORT_TYPE_WRITE"></span><span id="port_type_write"></span><dt>

<span data-ttu-id="15ecb-118">**埠 \_ 類型 \_ 寫入**</span><span class="sxs-lookup"><span data-stu-id="15ecb-118">**PORT\_TYPE\_WRITE**</span></span>
</dt><span id="PORT_TYPE_READ"></span><span id="port_type_read"></span><dt>

<span data-ttu-id="15ecb-119">**埠 \_ 類型 \_ 讀取**</span><span class="sxs-lookup"><span data-stu-id="15ecb-119">**PORT\_TYPE\_READ**</span></span>
</dt><span id="PORT_TYPE_REDIRECTED"></span><span id="port_type_redirected"></span><dt>

<span data-ttu-id="15ecb-120">**重新 \_ 導向的埠類型 \_**</span><span class="sxs-lookup"><span data-stu-id="15ecb-120">**PORT\_TYPE\_REDIRECTED**</span></span>
</dt><span id="PORT_TYPE_NET_ATTACHED"></span><span id="port_type_net_attached"></span><dt>

<span data-ttu-id="15ecb-121">**連接的埠 \_ 類型 \_ NET \_**</span><span class="sxs-lookup"><span data-stu-id="15ecb-121">**PORT\_TYPE\_NET\_ATTACHED**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="15ecb-122">**已保留**</span><span class="sxs-lookup"><span data-stu-id="15ecb-122">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="15ecb-123">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="15ecb-123">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15ecb-124">備註</span><span class="sxs-lookup"><span data-stu-id="15ecb-124">Remarks</span></span>

<span data-ttu-id="15ecb-125">如果已安裝多個支援相同埠的監視器，請在呼叫 [**EnumPorts**](enumports.md)時使用 **埠 \_ 資訊 \_ 2** 結構。</span><span class="sxs-lookup"><span data-stu-id="15ecb-125">Use the **PORT\_INFO\_2** structure when calling [**EnumPorts**](enumports.md) if there are multiple monitors installed that support the same ports.</span></span>

<span data-ttu-id="15ecb-126">您可以查詢 **fPortType** 成員，以判斷埠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="15ecb-126">The **fPortType** member can be queried to determine information about the port.</span></span> <span data-ttu-id="15ecb-127">請注意，通訊埠設定不會影響印表機資訊 (的 [印表機 [**\_ 資訊 \_**](printer-info-2.md) ]) 的 **屬性** 成員所傳回的印表機屬性。</span><span class="sxs-lookup"><span data-stu-id="15ecb-127">Note that port settings do not influence printer attributes (as returned by the **Attributes** member of [**PRINTER\_INFO\_2**](printer-info-2.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="15ecb-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="15ecb-128">Requirements</span></span>



| <span data-ttu-id="15ecb-129">需求</span><span class="sxs-lookup"><span data-stu-id="15ecb-129">Requirement</span></span> | <span data-ttu-id="15ecb-130">值</span><span class="sxs-lookup"><span data-stu-id="15ecb-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15ecb-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15ecb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="15ecb-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15ecb-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="15ecb-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15ecb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="15ecb-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15ecb-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="15ecb-135">標頭</span><span class="sxs-lookup"><span data-stu-id="15ecb-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="15ecb-136"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="15ecb-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="15ecb-137">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="15ecb-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="15ecb-138">**\_ 埠 \_ 資訊 \_ 2w** (Unicode) 和 **\_ 埠 \_ 資訊 \_ 2a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="15ecb-138">**\_PORT\_INFO\_2W** (Unicode) and **\_PORT\_INFO\_2A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="15ecb-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15ecb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15ecb-140">列印</span><span class="sxs-lookup"><span data-stu-id="15ecb-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="15ecb-141">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="15ecb-141">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="15ecb-142">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="15ecb-142">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




