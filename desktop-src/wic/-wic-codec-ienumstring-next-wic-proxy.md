---
description: Windows 影像處理元件 (WIC) proxy 函式用於 IEnumString：： Next。
ms.assetid: a3f6a32b-3043-4bea-a70b-0b4507b4e3a1
title: IEnumString_Next_WIC_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumString_Next_WIC_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ae3e25b355268fe63025692bf116b60b45122e76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026189"
---
# <a name="ienumstring_next_wic_proxy-function"></a><span data-ttu-id="ee912-103">IEnumString \_ 下一個 \_ WIC \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="ee912-103">IEnumString\_Next\_WIC\_Proxy function</span></span>

<span data-ttu-id="ee912-104">Windows 影像處理元件 (WIC) proxy 函式用於 IEnumString：： Next。</span><span class="sxs-lookup"><span data-stu-id="ee912-104">Windows Imaging Component (WIC) proxy function for IEnumString::Next.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee912-105">語法</span><span class="sxs-lookup"><span data-stu-id="ee912-105">Syntax</span></span>


```C++
HRESULT IEnumString_Next_WIC_Proxy(
  _In_ IEnumString *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="ee912-106">參數</span><span class="sxs-lookup"><span data-stu-id="ee912-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee912-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="ee912-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee912-108">類型： \**IEnumString \** _</span><span class="sxs-lookup"><span data-stu-id="ee912-108">Type: \**IEnumString\** _</span></span>

<span data-ttu-id="ee912-109">PARAMDESC</span><span class="sxs-lookup"><span data-stu-id="ee912-109">PARAMDESC</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee912-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee912-110">Return value</span></span>

<span data-ttu-id="ee912-111">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="ee912-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="ee912-112">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ee912-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ee912-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ee912-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee912-114">備註</span><span class="sxs-lookup"><span data-stu-id="ee912-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ee912-115">需求</span><span class="sxs-lookup"><span data-stu-id="ee912-115">Requirements</span></span>



| <span data-ttu-id="ee912-116">需求</span><span class="sxs-lookup"><span data-stu-id="ee912-116">Requirement</span></span> | <span data-ttu-id="ee912-117">值</span><span class="sxs-lookup"><span data-stu-id="ee912-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee912-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee912-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ee912-119">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee912-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ee912-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee912-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ee912-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee912-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ee912-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ee912-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee912-123"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee912-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




