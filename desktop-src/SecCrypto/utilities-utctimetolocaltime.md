---
description: 將國際標準時間 (格林尼治平均時間) 轉換為電腦的當地時間。
ms.assetid: 4085d7cb-d346-477d-a043-e96fb951c35a
title: UTCTimeToLocalTime 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.UTCTimeToLocalTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fe41cf8d9ec92c0c71be5130aded0b7db539b9b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000648"
---
# <a name="utilitiesutctimetolocaltime-method"></a><span data-ttu-id="e0d3c-103">UTCTimeToLocalTime 方法</span><span class="sxs-lookup"><span data-stu-id="e0d3c-103">Utilities.UTCTimeToLocalTime method</span></span>

<span data-ttu-id="e0d3c-104">\[**UTCTimeToLocalTime** 方法可用於 [需求] 區段中指定的作業系統。\]</span><span class="sxs-lookup"><span data-stu-id="e0d3c-104">\[The **UTCTimeToLocalTime** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="e0d3c-105">**UTCTimeToLocalTime** 方法會將國際標準時間的 (格林威治標準時間) 轉換為電腦的當地時間。</span><span class="sxs-lookup"><span data-stu-id="e0d3c-105">The **UTCTimeToLocalTime** method converts Coordinated Universal Time (Greenwich Mean Time) to the computer's local time.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0d3c-106">語法</span><span class="sxs-lookup"><span data-stu-id="e0d3c-106">Syntax</span></span>


```VB
Utilities.UTCTimeToLocalTime( _
  ByVal UTCTime _
)
```



## <a name="parameters"></a><span data-ttu-id="e0d3c-107">參數</span><span class="sxs-lookup"><span data-stu-id="e0d3c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0d3c-108">*UTCTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e0d3c-108">*UTCTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0d3c-109">要轉換為電腦本地時間的國際標準時間。</span><span class="sxs-lookup"><span data-stu-id="e0d3c-109">The Coordinated Universal Time to be converted to the computer's local time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0d3c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e0d3c-110">Return value</span></span>

<span data-ttu-id="e0d3c-111">對應至指定之國際標準時間的當地時間。</span><span class="sxs-lookup"><span data-stu-id="e0d3c-111">The local time that corresponds to the specified Coordinated Universal Time.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0d3c-112">備註</span><span class="sxs-lookup"><span data-stu-id="e0d3c-112">Remarks</span></span>

<span data-ttu-id="e0d3c-113">當系統在內部使用國際標準時間時，應用程式通常會顯示本地時間，也就是電腦本地時區的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="e0d3c-113">While the system uses Coordinated Universal Time internally, applications generally display the local time, which is the date and time of day for the computer's local time zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0d3c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0d3c-114">Requirements</span></span>



| <span data-ttu-id="e0d3c-115">需求</span><span class="sxs-lookup"><span data-stu-id="e0d3c-115">Requirement</span></span> | <span data-ttu-id="e0d3c-116">值</span><span class="sxs-lookup"><span data-stu-id="e0d3c-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0d3c-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="e0d3c-117">Redistributable</span></span><br/> | <span data-ttu-id="e0d3c-118">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e0d3c-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e0d3c-119">DLL</span><span class="sxs-lookup"><span data-stu-id="e0d3c-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="e0d3c-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0d3c-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0d3c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0d3c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0d3c-122">**公用程式**</span><span class="sxs-lookup"><span data-stu-id="e0d3c-122">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




