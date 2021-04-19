---
description: 將電腦的當地時間轉換成國際標準時間 (格林尼治平均時間) 。
ms.assetid: ff5d40ba-7d94-4f11-9c18-e41752d1d7b9
title: LocalTimeToUTCTime 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.LocalTimeToUTCTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2691e3306a84ce4eff3d73df4b070ba4b65671f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981261"
---
# <a name="utilitieslocaltimetoutctime-method"></a><span data-ttu-id="4982e-103">LocalTimeToUTCTime 方法</span><span class="sxs-lookup"><span data-stu-id="4982e-103">Utilities.LocalTimeToUTCTime method</span></span>

<span data-ttu-id="4982e-104">\[**LocalTimeToUTCTime** 方法可用於 [需求] 區段中指定的作業系統。\]</span><span class="sxs-lookup"><span data-stu-id="4982e-104">\[The **LocalTimeToUTCTime** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="4982e-105">**LocalTimeToUTCTime** 方法會將電腦的當地時間轉換成國際標準時間 (格林尼治平均時間) 。</span><span class="sxs-lookup"><span data-stu-id="4982e-105">The **LocalTimeToUTCTime** method converts the computer's local time to Coordinated Universal Time (Greenwich Mean Time).</span></span>

## <a name="syntax"></a><span data-ttu-id="4982e-106">語法</span><span class="sxs-lookup"><span data-stu-id="4982e-106">Syntax</span></span>


```VB
Utilities.LocalTimeToUTCTime( _
  ByVal LocalTime _
)
```



## <a name="parameters"></a><span data-ttu-id="4982e-107">參數</span><span class="sxs-lookup"><span data-stu-id="4982e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4982e-108">*LocalTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4982e-108">*LocalTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4982e-109">要轉換成國際標準時間的當地時間。</span><span class="sxs-lookup"><span data-stu-id="4982e-109">The local time to be converted to Coordinated Universal Time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4982e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4982e-110">Return value</span></span>

<span data-ttu-id="4982e-111">對應到指定之本地時間的國際標準時間。</span><span class="sxs-lookup"><span data-stu-id="4982e-111">The Coordinated Universal Time that corresponds to the specified local time.</span></span>

## <a name="remarks"></a><span data-ttu-id="4982e-112">備註</span><span class="sxs-lookup"><span data-stu-id="4982e-112">Remarks</span></span>

<span data-ttu-id="4982e-113">當系統在內部使用國際標準時間時，應用程式通常會顯示本地時間，也就是電腦本地時區的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="4982e-113">While the system uses Coordinated Universal Time internally, applications generally display the local time, which is the date and time of day for the computer's local time zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="4982e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="4982e-114">Requirements</span></span>



| <span data-ttu-id="4982e-115">需求</span><span class="sxs-lookup"><span data-stu-id="4982e-115">Requirement</span></span> | <span data-ttu-id="4982e-116">值</span><span class="sxs-lookup"><span data-stu-id="4982e-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4982e-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="4982e-117">Redistributable</span></span><br/> | <span data-ttu-id="4982e-118">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="4982e-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4982e-119">DLL</span><span class="sxs-lookup"><span data-stu-id="4982e-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="4982e-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4982e-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4982e-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4982e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4982e-122">**公用程式**</span><span class="sxs-lookup"><span data-stu-id="4982e-122">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




