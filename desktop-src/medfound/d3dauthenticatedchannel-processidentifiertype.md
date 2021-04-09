---
description: 指定 D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS 輸出結構中所識別的進程類型 \_ 。
ms.assetid: 8878905e-f55b-4dbc-9608-da0082daf673
title: 'D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE 列舉 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1b2fdb7384ff868b02f54650de9662b297ce39db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111821"
---
# <a name="d3dauthenticatedchannel_processidentifiertype-enumeration"></a><span data-ttu-id="823dc-103">D3DAUTHENTICATEDCHANNEL \_ PROCESSIDENTIFIERTYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="823dc-103">D3DAUTHENTICATEDCHANNEL\_PROCESSIDENTIFIERTYPE enumeration</span></span>

<span data-ttu-id="823dc-104">指定 [**D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ 輸出**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) 結構中所識別的進程類型。</span><span class="sxs-lookup"><span data-stu-id="823dc-104">Specifies the type of process that is identified in the [**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_OUTPUT**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="823dc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="823dc-105">Syntax</span></span>


```C++
typedef enum  { 
  PROCESSIDTYPE_UNKNOWN  = 0,
  PROCESSIDTYPE_DWM      = 1,
  PROCESSIDTYPE_HANDLE   = 2
} D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE;
```



## <a name="constants"></a><span data-ttu-id="823dc-106">常數</span><span class="sxs-lookup"><span data-stu-id="823dc-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="823dc-107"><span id="PROCESSIDTYPE_UNKNOWN"></span><span id="processidtype_unknown"></span>**PROCESSIDTYPE \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="823dc-107"><span id="PROCESSIDTYPE_UNKNOWN"></span><span id="processidtype_unknown"></span>**PROCESSIDTYPE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="823dc-108">未知的進程類型。</span><span class="sxs-lookup"><span data-stu-id="823dc-108">Unknown process type.</span></span>

</dd> <dt>

<span data-ttu-id="823dc-109"><span id="PROCESSIDTYPE_DWM"></span><span id="processidtype_dwm"></span>**PROCESSIDTYPE \_ DWM**</span><span class="sxs-lookup"><span data-stu-id="823dc-109"><span id="PROCESSIDTYPE_DWM"></span><span id="processidtype_dwm"></span>**PROCESSIDTYPE\_DWM**</span></span>
</dt> <dd>

<span data-ttu-id="823dc-110">桌面視窗管理員 (DWM) 進程。</span><span class="sxs-lookup"><span data-stu-id="823dc-110">Desktop Window Manager (DWM) process.</span></span>

</dd> <dt>

<span data-ttu-id="823dc-111"><span id="PROCESSIDTYPE_HANDLE"></span><span id="processidtype_handle"></span>**PROCESSIDTYPE \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="823dc-111"><span id="PROCESSIDTYPE_HANDLE"></span><span id="processidtype_handle"></span>**PROCESSIDTYPE\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="823dc-112">處理常式的控制碼。</span><span class="sxs-lookup"><span data-stu-id="823dc-112">Handle to a process.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="823dc-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="823dc-113">Requirements</span></span>



| <span data-ttu-id="823dc-114">需求</span><span class="sxs-lookup"><span data-stu-id="823dc-114">Requirement</span></span> | <span data-ttu-id="823dc-115">值</span><span class="sxs-lookup"><span data-stu-id="823dc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="823dc-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="823dc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="823dc-117">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="823dc-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="823dc-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="823dc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="823dc-119">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="823dc-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="823dc-120">標頭</span><span class="sxs-lookup"><span data-stu-id="823dc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="823dc-121"><dt>D3d9types (包含 D3d9) </dt></span><span class="sxs-lookup"><span data-stu-id="823dc-121"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="823dc-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="823dc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="823dc-123">Direct3D 影片列舉</span><span class="sxs-lookup"><span data-stu-id="823dc-123">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)
</dt> </dl>

 

 




