---
description: 判斷指定的資料庫是否為其中一個標準資料庫 (Sysmain、Apphelp、Drvmain 或 Msimain) 。
ms.assetid: 7d7e3ca7-535e-40b3-b635-299eff8abea5
title: SdbIsStandardDatabase 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbIsStandardDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9e9e445162c2bfc171ccf975981876f81a8bb804
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025813"
---
# <a name="sdbisstandarddatabase-function"></a><span data-ttu-id="bdf18-103">SdbIsStandardDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="bdf18-103">SdbIsStandardDatabase function</span></span>

<span data-ttu-id="bdf18-104">判斷指定的資料庫是否為其中一個標準資料庫 (Sysmain、Apphelp、Drvmain 或 Msimain) 。</span><span class="sxs-lookup"><span data-stu-id="bdf18-104">Determines whether the specified database is one of the standard databases (Sysmain, Apphelp, Drvmain, or Msimain).</span></span>

## <a name="syntax"></a><span data-ttu-id="bdf18-105">語法</span><span class="sxs-lookup"><span data-stu-id="bdf18-105">Syntax</span></span>


```C++
BOOL WINAPI SdbIsStandardDatabase(
  _In_ GUID GuidDB
);
```



## <a name="parameters"></a><span data-ttu-id="bdf18-106">參數</span><span class="sxs-lookup"><span data-stu-id="bdf18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdf18-107">*GuidDB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bdf18-107">*GuidDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf18-108">資料庫的 GUID。</span><span class="sxs-lookup"><span data-stu-id="bdf18-108">The GUID for the database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdf18-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="bdf18-109">Return value</span></span>

<span data-ttu-id="bdf18-110">如果 GUID 代表標準資料庫，則函式會傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="bdf18-110">The function returns **TRUE** if the GUID represents a standard database or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdf18-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="bdf18-111">Requirements</span></span>



| <span data-ttu-id="bdf18-112">需求</span><span class="sxs-lookup"><span data-stu-id="bdf18-112">Requirement</span></span> | <span data-ttu-id="bdf18-113">值</span><span class="sxs-lookup"><span data-stu-id="bdf18-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdf18-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bdf18-114">Minimum supported client</span></span><br/> | <span data-ttu-id="bdf18-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bdf18-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bdf18-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bdf18-116">Minimum supported server</span></span><br/> | <span data-ttu-id="bdf18-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bdf18-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bdf18-118">DLL</span><span class="sxs-lookup"><span data-stu-id="bdf18-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdf18-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdf18-119"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




