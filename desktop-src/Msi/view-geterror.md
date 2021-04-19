---
description: View 物件的 GetError 方法會傳回發生錯誤的驗證錯誤和資料行名稱。
ms.assetid: ca90dfa5-8e15-490c-835b-c5c225c3cc7b
title: GetError 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.GetError
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1305bf6f497e92ff4d455a696179a943df8a057b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990161"
---
# <a name="viewgeterror-method"></a><span data-ttu-id="30aae-103">GetError 方法</span><span class="sxs-lookup"><span data-stu-id="30aae-103">View.GetError method</span></span>

<span data-ttu-id="30aae-104">[**View**](view-object.md)物件的 **GetError** 方法會傳回發生錯誤的驗證錯誤和資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="30aae-104">The **GetError** method of the [**View**](view-object.md) object returns the Validation error and the column name for which the error occurred.</span></span> <span data-ttu-id="30aae-105">在自動化中，傳回的值為 ColumnName 形式的字串 \# \# ，其中 \# \# 代表2位數的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="30aae-105">In automation, the returned value is a string of the form \#\#ColumnName, where the \#\# represents a 2-digit error code.</span></span> <span data-ttu-id="30aae-106">它會傳回視圖錯誤陣列中的第一個錯誤;後續呼叫會傳回錯誤陣列中的下一個值。</span><span class="sxs-lookup"><span data-stu-id="30aae-106">It returns the first error in the view's error array; subsequent calls return the next value in the error array.</span></span> <span data-ttu-id="30aae-107">一旦傳回 ' 00 ' 的值，就不會有其他錯誤存在，而且後續的呼叫只會再次迴圈執行陣列。</span><span class="sxs-lookup"><span data-stu-id="30aae-107">Once a value of '00' is returned, no more errors exist, and subsequent calls merely loop through the array again.</span></span>

## <a name="syntax"></a><span data-ttu-id="30aae-108">語法</span><span class="sxs-lookup"><span data-stu-id="30aae-108">Syntax</span></span>


```JScript
View.GetError()
```



## <a name="parameters"></a><span data-ttu-id="30aae-109">參數</span><span class="sxs-lookup"><span data-stu-id="30aae-109">Parameters</span></span>

<span data-ttu-id="30aae-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="30aae-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="30aae-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="30aae-111">Return value</span></span>

<span data-ttu-id="30aae-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="30aae-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="30aae-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="30aae-113">Requirements</span></span>



| <span data-ttu-id="30aae-114">需求</span><span class="sxs-lookup"><span data-stu-id="30aae-114">Requirement</span></span> | <span data-ttu-id="30aae-115">值</span><span class="sxs-lookup"><span data-stu-id="30aae-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30aae-116">版本</span><span class="sxs-lookup"><span data-stu-id="30aae-116">Version</span></span><br/> | <span data-ttu-id="30aae-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="30aae-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="30aae-118">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="30aae-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="30aae-119">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="30aae-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="30aae-120">DLL</span><span class="sxs-lookup"><span data-stu-id="30aae-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="30aae-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30aae-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="30aae-122">IID</span><span class="sxs-lookup"><span data-stu-id="30aae-122">IID</span></span><br/>     | <span data-ttu-id="30aae-123">IID \_ IView 定義為 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="30aae-123">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




