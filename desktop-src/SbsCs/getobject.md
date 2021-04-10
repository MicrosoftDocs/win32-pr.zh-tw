---
description: GetObject 方法會取得現有 ActCtx 物件的實例。
ms.assetid: 547525f3-afef-463b-823a-df8ccd954f36
title: ActCtx 的 GetObject 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.GetObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 11b71d8d40d947472612c91f70e9956aa7798806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690159"
---
# <a name="actctxgetobject-method"></a><span data-ttu-id="13d26-103">ActCtx 的 GetObject 方法</span><span class="sxs-lookup"><span data-stu-id="13d26-103">ActCtx.GetObject method</span></span>

<span data-ttu-id="13d26-104">**GetObject** 方法會取得現有 [**ActCtx**](microsoft-windows-actctx-object.md)物件的實例。</span><span class="sxs-lookup"><span data-stu-id="13d26-104">The **GetObject** method gets an instance of an existing [**Microsoft.Windows.ActCtx**](microsoft-windows-actctx-object.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="13d26-105">語法</span><span class="sxs-lookup"><span data-stu-id="13d26-105">Syntax</span></span>


```JScript
ActCtx.GetObject(
  bstrName
)
```



## <a name="parameters"></a><span data-ttu-id="13d26-106">參數</span><span class="sxs-lookup"><span data-stu-id="13d26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13d26-107">*bstrName*</span><span class="sxs-lookup"><span data-stu-id="13d26-107">*bstrName*</span></span> 
</dt> <dd>

<span data-ttu-id="13d26-108">表示物件的必要字串。</span><span class="sxs-lookup"><span data-stu-id="13d26-108">Required string that indicates the object.</span></span> <span data-ttu-id="13d26-109">此名稱必須位於 **HKEY \_ LOCAL \_ MACHINE** \\ **Microsoft** \\ **Visual Studio** \\ **6.0** \\ **<package>** \\ **Automation** 下的登錄中。</span><span class="sxs-lookup"><span data-stu-id="13d26-109">The name must be in the registry under **HKEY\_LOCAL\_MACHINE**\\**Microsoft**\\**Visual Studio**\\**6.0**\\**<package>**\\**Automation**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13d26-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="13d26-110">Return value</span></span>

<span data-ttu-id="13d26-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="13d26-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="13d26-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="13d26-112">Requirements</span></span>



| <span data-ttu-id="13d26-113">需求</span><span class="sxs-lookup"><span data-stu-id="13d26-113">Requirement</span></span> | <span data-ttu-id="13d26-114">值</span><span class="sxs-lookup"><span data-stu-id="13d26-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="13d26-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13d26-115">Minimum supported client</span></span><br/> | <span data-ttu-id="13d26-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13d26-116">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="13d26-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13d26-117">Minimum supported server</span></span><br/> | <span data-ttu-id="13d26-118">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13d26-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="13d26-119">DLL</span><span class="sxs-lookup"><span data-stu-id="13d26-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13d26-120"><dt>Sxsoa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13d26-120"><dt>Sxsoa.dll</dt></span></span> </dl> |
| <span data-ttu-id="13d26-121">IID</span><span class="sxs-lookup"><span data-stu-id="13d26-121">IID</span></span><br/>                      | <span data-ttu-id="13d26-122">IID \_ IActCtx 定義為8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span><span class="sxs-lookup"><span data-stu-id="13d26-122">IID\_IActCtx is defined as 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="13d26-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13d26-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13d26-124">**CreateObject 方法**</span><span class="sxs-lookup"><span data-stu-id="13d26-124">**CreateObject Method**</span></span>](createobject.md)
</dt> </dl>

 

 




