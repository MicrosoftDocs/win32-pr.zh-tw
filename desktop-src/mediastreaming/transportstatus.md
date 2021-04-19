---
title: TransportStatus 列舉
description: 定義 UPnP 指導方針所定義的可用傳輸狀態。
ms.assetid: 6fde82f0-9bc4-4abb-9d10-0000501c2b24
keywords:
- TransportStatus 列舉媒體串流 API
topic_type:
- apiref
api_name:
- TransportStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4a9de34f358db96b468dbd3329483a8e09b6b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996079"
---
# <a name="transportstatus-enumeration"></a><span data-ttu-id="1f874-104">TransportStatus 列舉</span><span class="sxs-lookup"><span data-stu-id="1f874-104">TransportStatus enumeration</span></span>

<span data-ttu-id="1f874-105">定義 UPnP 指導方針所定義的可用傳輸狀態。</span><span class="sxs-lookup"><span data-stu-id="1f874-105">Defines the available transport status as defined by the UPnP Guidelines.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f874-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f874-106">Syntax</span></span>


```C++
typedef enum TransportStatus { 
  Unknown        = 0,
  Ok             = 1,
  ErrorOccurred  = 2,
  Last           = 3
} TransportStatus;
```



## <a name="constants"></a><span data-ttu-id="1f874-107">常數</span><span class="sxs-lookup"><span data-stu-id="1f874-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1f874-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知**</span><span class="sxs-lookup"><span data-stu-id="1f874-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="1f874-109">錯誤的裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="1f874-109">Erroneous device status.</span></span>

</dd> <dt>

<span data-ttu-id="1f874-110"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**還行**</span><span class="sxs-lookup"><span data-stu-id="1f874-110"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Ok**</span></span>
</dt> <dd>

<span data-ttu-id="1f874-111">裝置處於良好狀態。</span><span class="sxs-lookup"><span data-stu-id="1f874-111">The device is in a good status.</span></span>

</dd> <dt>

<span data-ttu-id="1f874-112"><span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**ErrorOccurred**</span><span class="sxs-lookup"><span data-stu-id="1f874-112"><span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**ErrorOccurred**</span></span>
</dt> <dd>

<span data-ttu-id="1f874-113">裝置發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="1f874-113">An error occurred on the device.</span></span>

</dd> <dt>

<span data-ttu-id="1f874-114"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**最後**</span><span class="sxs-lookup"><span data-stu-id="1f874-114"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Last**</span></span>
</dt> <dd>

<span data-ttu-id="1f874-115">裝置的先前狀態為目前的傳輸狀態。</span><span class="sxs-lookup"><span data-stu-id="1f874-115">The device s previous status to the current transport status.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f874-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f874-116">Requirements</span></span>



| <span data-ttu-id="1f874-117">需求</span><span class="sxs-lookup"><span data-stu-id="1f874-117">Requirement</span></span> | <span data-ttu-id="1f874-118">值</span><span class="sxs-lookup"><span data-stu-id="1f874-118">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f874-119">Idl</span><span class="sxs-lookup"><span data-stu-id="1f874-119">IDL</span></span><br/> | <dl> <span data-ttu-id="1f874-120"><dt> (參考) 的 windows...。 </dt></span><span class="sxs-lookup"><span data-stu-id="1f874-120"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





