---
description: GetMaximumCursors 方法會抓取 tablet 裝置支援的最大資料指標數目。
ms.assetid: 5a43d792-e64c-4506-9792-31efe0885959
title: ITablet3：： GetMaximumCursors 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.GetMaximumCursors
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 7c40184d35ac1d42cb5f5e845396b40efc2d928e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976960"
---
# <a name="itablet3getmaximumcursors-method"></a><span data-ttu-id="6a35e-103">ITablet3：： GetMaximumCursors 方法</span><span class="sxs-lookup"><span data-stu-id="6a35e-103">ITablet3::GetMaximumCursors method</span></span>

<span data-ttu-id="6a35e-104">**GetMaximumCursors** 方法會抓取 tablet 裝置支援的最大資料指標數目。</span><span class="sxs-lookup"><span data-stu-id="6a35e-104">The **GetMaximumCursors** method retrieves the maximum number of cursors that a tablet device supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a35e-105">語法</span><span class="sxs-lookup"><span data-stu-id="6a35e-105">Syntax</span></span>


```C++
HRESULT GetMaximumCursors(
   ULONG *pMaximumCursors
);
```



## <a name="parameters"></a><span data-ttu-id="6a35e-106">參數</span><span class="sxs-lookup"><span data-stu-id="6a35e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a35e-107">*pMaximumCursors*</span><span class="sxs-lookup"><span data-stu-id="6a35e-107">*pMaximumCursors*</span></span> 
</dt> <dd>

<span data-ttu-id="6a35e-108">裝置支援的輸入數目上限。</span><span class="sxs-lookup"><span data-stu-id="6a35e-108">The maximum number of inputs that the device supports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a35e-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a35e-109">Return value</span></span>

<span data-ttu-id="6a35e-110">\_成功時傳回 S OK，否則傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6a35e-110">Returns S\_OK on success; otherwise, returns an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a35e-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a35e-111">Requirements</span></span>



| <span data-ttu-id="6a35e-112">需求</span><span class="sxs-lookup"><span data-stu-id="6a35e-112">Requirement</span></span> | <span data-ttu-id="6a35e-113">值</span><span class="sxs-lookup"><span data-stu-id="6a35e-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a35e-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6a35e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6a35e-115">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a35e-115">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6a35e-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6a35e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6a35e-117">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a35e-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6a35e-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="6a35e-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="6a35e-119"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6a35e-119"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a35e-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a35e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a35e-121">**ITablet3**</span><span class="sxs-lookup"><span data-stu-id="6a35e-121">**ITablet3**</span></span>](itablet3.md)
</dt> </dl>

 

 




