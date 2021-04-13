---
title: 'MMIOM_CLOSE 訊息 (Mmsystem .h) '
description: MmioClose 函 \_ 式會將 MMIOM CLOSE 訊息傳送至 i/o 程式，以要求關閉檔案。
ms.assetid: 9d0dad5b-fd0a-4948-a4cf-9d138e353c76
keywords:
- MMIOM_CLOSE message Windows 多媒體
topic_type:
- apiref
api_name:
- MMIOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7863698b99bcead8bc22e6194d213bbc663d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509486"
---
# <a name="mmiom_close-message"></a><span data-ttu-id="80e4b-104">MMIOM \_ 關閉訊息</span><span class="sxs-lookup"><span data-stu-id="80e4b-104">MMIOM\_CLOSE message</span></span>

<span data-ttu-id="80e4b-105">[**MmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)函式會將 **MMIOM \_ CLOSE** 訊息傳送至 i/o 程式，以要求關閉檔案。</span><span class="sxs-lookup"><span data-stu-id="80e4b-105">The **MMIOM\_CLOSE** message is sent to an I/O procedure by the [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) function to request that a file be closed.</span></span>


```C++
MMIOM_CLOSE 
lParam1 = (LPARAM) lCloseFlags 
lParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="80e4b-106">參數</span><span class="sxs-lookup"><span data-stu-id="80e4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80e4b-107"><span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*lCloseFlags*</span><span class="sxs-lookup"><span data-stu-id="80e4b-107"><span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*lCloseFlags*</span></span>
</dt> <dd>

<span data-ttu-id="80e4b-108">**MmioClose** 的 **wFlags** 參數中所包含的旗標。</span><span class="sxs-lookup"><span data-stu-id="80e4b-108">Flags contained in the **wFlags** parameter of **mmioClose**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80e4b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="80e4b-109">Return Value</span></span>

<span data-ttu-id="80e4b-110">如果檔案已成功關閉，則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="80e4b-110">Returns zero if the file is successfully closed or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="80e4b-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="80e4b-111">Requirements</span></span>



| <span data-ttu-id="80e4b-112">需求</span><span class="sxs-lookup"><span data-stu-id="80e4b-112">Requirement</span></span> | <span data-ttu-id="80e4b-113">值</span><span class="sxs-lookup"><span data-stu-id="80e4b-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80e4b-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80e4b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="80e4b-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80e4b-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="80e4b-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80e4b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="80e4b-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80e4b-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="80e4b-118">標頭</span><span class="sxs-lookup"><span data-stu-id="80e4b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="80e4b-119"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="80e4b-119"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

