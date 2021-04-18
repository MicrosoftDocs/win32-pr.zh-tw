---
title: 'TYPEMODE 列舉 (Softkbdc) '
description: TYPEMODE 列舉的元素可用來指定可供軟鍵盤使用的類型模式。
ms.assetid: 7db0a4dd-0ee2-455d-aeb8-11cd1249134c
keywords:
- TYPEMODE 列舉文字服務架構
topic_type:
- apiref
api_name:
- TYPEMODE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24054443802d0b8a759841cb6b3fc3cb5d510024
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967321"
---
# <a name="typemode-enumeration"></a><span data-ttu-id="6d185-104">TYPEMODE 列舉</span><span class="sxs-lookup"><span data-stu-id="6d185-104">TYPEMODE enumeration</span></span>

<span data-ttu-id="6d185-105">**TYPEMODE** 列舉的元素可用來指定可供軟鍵盤使用的類型模式。</span><span class="sxs-lookup"><span data-stu-id="6d185-105">Elements of the **TYPEMODE** enumeration are used to specify type modes that are available for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d185-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d185-106">Syntax</span></span>


```C++
typedef enum tagTYPEMODE { 
  ClickMouse  = 0,
  Hover       = 1,
  Scanning    = 2
} TYPEMODE;
```



## <a name="constants"></a><span data-ttu-id="6d185-107">常數</span><span class="sxs-lookup"><span data-stu-id="6d185-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6d185-108"><span id="ClickMouse"></span><span id="clickmouse"></span><span id="CLICKMOUSE"></span>**ClickMouse**</span><span class="sxs-lookup"><span data-stu-id="6d185-108"><span id="ClickMouse"></span><span id="clickmouse"></span><span id="CLICKMOUSE"></span>**ClickMouse**</span></span>
</dt> <dd>

<span data-ttu-id="6d185-109">使用者可以按一下螢幕上的按鍵來輸入文字。</span><span class="sxs-lookup"><span data-stu-id="6d185-109">The user can click the on-screen keys to type text.</span></span>

</dd> <dt>

<span data-ttu-id="6d185-110"><span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**懸停**</span><span class="sxs-lookup"><span data-stu-id="6d185-110"><span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**Hover**</span></span>
</dt> <dd>

<span data-ttu-id="6d185-111">使用者可以在預先定義的時間點指向金鑰，而選取的字元會自動輸入。</span><span class="sxs-lookup"><span data-stu-id="6d185-111">The user can point to a key for a predefined period of time, and the selected character is typed automatically.</span></span>

</dd> <dt>

<span data-ttu-id="6d185-112"><span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**掃描**</span><span class="sxs-lookup"><span data-stu-id="6d185-112"><span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**Scanning**</span></span>
</dt> <dd>

<span data-ttu-id="6d185-113">軟鍵盤會持續掃描輸入區域，並反白顯示使用者可以按下快速鍵或使用切換輸入裝置的區域。</span><span class="sxs-lookup"><span data-stu-id="6d185-113">The soft keyboard continually scans the input area and highlights regions where the user can press a shortcut key or use a switch-input device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d185-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d185-114">Requirements</span></span>



| <span data-ttu-id="6d185-115">需求</span><span class="sxs-lookup"><span data-stu-id="6d185-115">Requirement</span></span> | <span data-ttu-id="6d185-116">值</span><span class="sxs-lookup"><span data-stu-id="6d185-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d185-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6d185-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6d185-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d185-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6d185-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6d185-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6d185-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d185-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6d185-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="6d185-121">Redistributable</span></span><br/>          | <span data-ttu-id="6d185-122">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="6d185-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="6d185-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6d185-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d185-124"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="6d185-124"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="6d185-125">Idl</span><span class="sxs-lookup"><span data-stu-id="6d185-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6d185-126"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6d185-126"><dt>Softkbd.idl</dt></span></span> </dl> |



 

 





