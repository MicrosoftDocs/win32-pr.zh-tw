---
description: 在列舉可用的 IWiaItem2 物件期間略過指定數目的專案。
ms.assetid: 7a5e9e1c-1e6e-4de0-9499-bf89e35c19aa
title: 'IEnumWiaItem2：： Skip 方法 (Wia. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Skip
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7618aad923136a9a32d8b7fb935050fefe07bff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943588"
---
# <a name="ienumwiaitem2skip-method"></a><span data-ttu-id="61379-103">IEnumWiaItem2：： Skip 方法</span><span class="sxs-lookup"><span data-stu-id="61379-103">IEnumWiaItem2::Skip method</span></span>

<span data-ttu-id="61379-104">在列舉可用的 [**IWiaItem2**](-wia-iwiaitem2.md) 物件期間略過指定數目的專案。</span><span class="sxs-lookup"><span data-stu-id="61379-104">Skips the specified number of items during an enumeration of available [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="61379-105">語法</span><span class="sxs-lookup"><span data-stu-id="61379-105">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG cElt
);
```



## <a name="parameters"></a><span data-ttu-id="61379-106">參數</span><span class="sxs-lookup"><span data-stu-id="61379-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61379-107">*cElt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61379-107">*cElt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61379-108">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="61379-108">Type: **ULONG**</span></span>

<span data-ttu-id="61379-109">指定要略過的專案數。</span><span class="sxs-lookup"><span data-stu-id="61379-109">Specifies the number of items to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61379-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="61379-110">Return value</span></span>

<span data-ttu-id="61379-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="61379-111">Type: **HRESULT**</span></span>

<span data-ttu-id="61379-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="61379-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="61379-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="61379-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="61379-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="61379-114">Requirements</span></span>



| <span data-ttu-id="61379-115">需求</span><span class="sxs-lookup"><span data-stu-id="61379-115">Requirement</span></span> | <span data-ttu-id="61379-116">值</span><span class="sxs-lookup"><span data-stu-id="61379-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="61379-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61379-117">Minimum supported client</span></span><br/> | <span data-ttu-id="61379-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61379-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="61379-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61379-119">Minimum supported server</span></span><br/> | <span data-ttu-id="61379-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61379-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="61379-121">標頭</span><span class="sxs-lookup"><span data-stu-id="61379-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="61379-122"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="61379-122"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="61379-123">Idl</span><span class="sxs-lookup"><span data-stu-id="61379-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="61379-124"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="61379-124"><dt>Wia.idl</dt></span></span> </dl> |



 

 




