---
description: 載入 Apphelp 資源檔。
ms.assetid: fca50e00-9324-410a-a572-69441f332593
title: SdbOpenApphelpResourceFile 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpResourceFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2f1dfb1695e25bfb82e01ffa4f9eac4e245a6ffa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385933"
---
# <a name="sdbopenapphelpresourcefile-function"></a><span data-ttu-id="bbef8-103">SdbOpenApphelpResourceFile 函式</span><span class="sxs-lookup"><span data-stu-id="bbef8-103">SdbOpenApphelpResourceFile function</span></span>

<span data-ttu-id="bbef8-104">載入 Apphelp 資源檔。</span><span class="sxs-lookup"><span data-stu-id="bbef8-104">Loads the Apphelp resource file.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbef8-105">語法</span><span class="sxs-lookup"><span data-stu-id="bbef8-105">Syntax</span></span>


```C++
HMODULE WINAPI SdbOpenApphelpResourceFile(
  _In_opt_ LPCWSTR pwszACResourceFile
);
```



## <a name="parameters"></a><span data-ttu-id="bbef8-106">參數</span><span class="sxs-lookup"><span data-stu-id="bbef8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbef8-107">*pwszACResourceFile* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="bbef8-107">*pwszACResourceFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bbef8-108">資源檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="bbef8-108">The path to the resource file.</span></span> <span data-ttu-id="bbef8-109">如果此參數為 **Null**，則會開啟本機資源 DLL。</span><span class="sxs-lookup"><span data-stu-id="bbef8-109">If this parameter is **NULL**, the local resource DLL is opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbef8-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="bbef8-110">Return value</span></span>

<span data-ttu-id="bbef8-111">函式會將控制碼傳回至已開啟的資源檔。</span><span class="sxs-lookup"><span data-stu-id="bbef8-111">The function returns a handle to the opened resource file.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbef8-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="bbef8-112">Requirements</span></span>



| <span data-ttu-id="bbef8-113">需求</span><span class="sxs-lookup"><span data-stu-id="bbef8-113">Requirement</span></span> | <span data-ttu-id="bbef8-114">值</span><span class="sxs-lookup"><span data-stu-id="bbef8-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbef8-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bbef8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bbef8-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bbef8-116">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bbef8-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bbef8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bbef8-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bbef8-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bbef8-119">DLL</span><span class="sxs-lookup"><span data-stu-id="bbef8-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbef8-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbef8-120"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




