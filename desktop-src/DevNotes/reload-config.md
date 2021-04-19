---
description: 只以日文 IME 重載 HKCU 登錄中的 IME 設定。
ms.assetid: 171c31ad-c925-4e18-b458-d9abf52dae9a
title: reload_config 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- reload_config
api_type:
- DllExport
api_location:
- Imejpknl.dll
- Imejp98k.dll
ms.openlocfilehash: bc9d0d026359036d8847ebaa2542f778de4d5767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987950"
---
# <a name="reload_config-function"></a><span data-ttu-id="d0130-103">重載 \_ config 函數</span><span class="sxs-lookup"><span data-stu-id="d0130-103">reload\_config function</span></span>

<span data-ttu-id="d0130-104">只以日文 IME 重載 HKCU 登錄中的 IME 設定。</span><span class="sxs-lookup"><span data-stu-id="d0130-104">Reloads an IME configuration from the HKCU registry, in Japanese IME only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0130-105">語法</span><span class="sxs-lookup"><span data-stu-id="d0130-105">Syntax</span></span>


```C++
BOOL reload_config(void);
```



## <a name="parameters"></a><span data-ttu-id="d0130-106">參數</span><span class="sxs-lookup"><span data-stu-id="d0130-106">Parameters</span></span>

<span data-ttu-id="d0130-107">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="d0130-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d0130-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0130-108">Return value</span></span>

<span data-ttu-id="d0130-109">如果成功，則此函式會傳回 **TRUE** ;否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d0130-109">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0130-110">備註</span><span class="sxs-lookup"><span data-stu-id="d0130-110">Remarks</span></span>

<span data-ttu-id="d0130-111">如果 HKCU 中沒有任何登錄值，則 **重載設定 \_** 函數會將初始資料寫入至登錄。</span><span class="sxs-lookup"><span data-stu-id="d0130-111">If no registry value is present in HKCU, the **reload\_config** function writes initial data to the registry.</span></span>

<span data-ttu-id="d0130-112">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="d0130-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0130-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0130-113">Requirements</span></span>



| <span data-ttu-id="d0130-114">需求</span><span class="sxs-lookup"><span data-stu-id="d0130-114">Requirement</span></span> | <span data-ttu-id="d0130-115">值</span><span class="sxs-lookup"><span data-stu-id="d0130-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0130-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d0130-116">DLL</span></span><br/> | <dl> <span data-ttu-id="d0130-117"><dt>Imejpknl.dll;</dt><dt>Imejp98k.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0130-117"><dt>Imejpknl.dll; </dt> <dt>Imejp98k.dll</dt></span></span> </dl> |



 

 
