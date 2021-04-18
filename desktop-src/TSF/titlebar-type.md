---
title: 'TITLEBAR_TYPE 列舉 (Softkbdc .h) '
description: 標題列型別 \_ 列舉的元素是用來指定可供軟鍵盤視窗使用的 titlebars 類型。
ms.assetid: 10d9b1c0-fd52-4f62-9268-cb8903a4c2db
keywords:
- TITLEBAR_TYPE 列舉文字服務架構
topic_type:
- apiref
api_name:
- TITLEBAR_TYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97ae1af1aba106a9f319cee080d0963992034a75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965087"
---
# <a name="titlebar_type-enumeration"></a><span data-ttu-id="a7658-104">標題列 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="a7658-104">TITLEBAR\_TYPE enumeration</span></span>

<span data-ttu-id="a7658-105">**標題列 \_ 型** 別列舉的元素是用來指定可供軟鍵盤視窗使用的 titlebars 類型。</span><span class="sxs-lookup"><span data-stu-id="a7658-105">Elements of the **TITLEBAR\_TYPE** enumeration are used to specify types of titlebars that are available for a soft keyboard window.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7658-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7658-106">Syntax</span></span>


```C++
typedef enum tagTITLEBAR_TYPE { 
  TITLEBAR_NONE                = 0,
  TITLEBAR_GRIPPER_HORIZ_ONLY  = 1,
  TITLEBAR_GRIPPER_VERTI_ONLY  = 2,
  TITLEBAR_GRIPPER_BUTTON      = 3
} TITLEBAR_TYPE;
```



## <a name="constants"></a><span data-ttu-id="a7658-107">常數</span><span class="sxs-lookup"><span data-stu-id="a7658-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a7658-108"><span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**標題列 \_ 無**</span><span class="sxs-lookup"><span data-stu-id="a7658-108"><span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**TITLEBAR\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="a7658-109">[螢幕小鍵盤] 視窗不會使用標題列。</span><span class="sxs-lookup"><span data-stu-id="a7658-109">The soft keyboard window uses no titlebar.</span></span>

</dd> <dt>

<span data-ttu-id="a7658-110"><span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**標題 \_ 欄 \_ \_ 僅限水準控制**</span><span class="sxs-lookup"><span data-stu-id="a7658-110"><span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**TITLEBAR\_GRIPPER\_HORIZ\_ONLY**</span></span>
</dt> <dd>

<span data-ttu-id="a7658-111">[螢幕小鍵盤] 視窗只會使用水準移出控制條。</span><span class="sxs-lookup"><span data-stu-id="a7658-111">The soft keyboard window uses a horizontal gripper bar only.</span></span>

</dd> <dt>

<span data-ttu-id="a7658-112"><span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**標題列 \_ 抓取 \_ VERTI \_**</span><span class="sxs-lookup"><span data-stu-id="a7658-112"><span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**TITLEBAR\_GRIPPER\_VERTI\_ONLY**</span></span>
</dt> <dd>

<span data-ttu-id="a7658-113">[螢幕小鍵盤] 視窗只會使用垂直的控制手柄列。</span><span class="sxs-lookup"><span data-stu-id="a7658-113">The soft keyboard window uses a vertical gripper bar only.</span></span>

</dd> <dt>

<span data-ttu-id="a7658-114"><span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**標題列 \_ 抓取 \_ 按鈕**</span><span class="sxs-lookup"><span data-stu-id="a7658-114"><span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**TITLEBAR\_GRIPPER\_BUTTON**</span></span>
</dt> <dd>

<span data-ttu-id="a7658-115">[螢幕小鍵盤] 視窗只會使用 [移出控制] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a7658-115">The soft keyboard window uses a gripper button only.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a7658-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7658-116">Requirements</span></span>



| <span data-ttu-id="a7658-117">需求</span><span class="sxs-lookup"><span data-stu-id="a7658-117">Requirement</span></span> | <span data-ttu-id="a7658-118">值</span><span class="sxs-lookup"><span data-stu-id="a7658-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7658-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7658-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a7658-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7658-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a7658-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7658-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a7658-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7658-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a7658-123">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="a7658-123">Redistributable</span></span><br/>          | <span data-ttu-id="a7658-124">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="a7658-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="a7658-125">標頭</span><span class="sxs-lookup"><span data-stu-id="a7658-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7658-126"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="a7658-126"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="a7658-127">Idl</span><span class="sxs-lookup"><span data-stu-id="a7658-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a7658-128"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7658-128"><dt>Softkbd.idl</dt></span></span> </dl> |



 

 





