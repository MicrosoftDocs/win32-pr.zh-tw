---
title: 'MCI_OVLY_OPEN_PARMS 結構 (Mmsystem .h) '
description: MCI \_ OVLY \_ OPEN \_ PARMS 結構包含適用于影片重迭裝置的 mci \_ OPEN 命令資訊。
ms.assetid: 1559ae40-4aa5-4dfc-b337-7b056c706b67
keywords:
- MCI_OVLY_OPEN_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_OVLY_OPEN_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e64b864b4b0366421828960504aff3f5a83836b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464228"
---
# <a name="mci_ovly_open_parms-structure"></a><span data-ttu-id="268ff-104">MCI \_ OVLY \_ 開啟 \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="268ff-104">MCI\_OVLY\_OPEN\_PARMS structure</span></span>

<span data-ttu-id="268ff-105">**Mci \_ OVLY \_ OPEN \_ PARMS** 結構包含適用于影片重迭裝置的 [**mci \_ OPEN**](mci-open.md)命令資訊。</span><span class="sxs-lookup"><span data-stu-id="268ff-105">The **MCI\_OVLY\_OPEN\_PARMS** structure contains information for the [**MCI\_OPEN**](mci-open.md) command for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="268ff-106">語法</span><span class="sxs-lookup"><span data-stu-id="268ff-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwStyle;
  DWORD       hWndParent;
} MCI_OVLY_OPEN_PARMS;
```



## <a name="members"></a><span data-ttu-id="268ff-107">成員</span><span class="sxs-lookup"><span data-stu-id="268ff-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="268ff-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="268ff-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="268ff-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="268ff-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="268ff-110">**wDeviceID**</span><span class="sxs-lookup"><span data-stu-id="268ff-110">**wDeviceID**</span></span>
</dt> <dd>

<span data-ttu-id="268ff-111">傳回給應用程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="268ff-111">Identifier returned to application.</span></span>

</dd> <dt>

<span data-ttu-id="268ff-112">**lpstrDeviceType**</span><span class="sxs-lookup"><span data-stu-id="268ff-112">**lpstrDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="268ff-113">裝置類型的名稱或常數識別碼。</span><span class="sxs-lookup"><span data-stu-id="268ff-113">Name or constant identifier of the device type.</span></span> <span data-ttu-id="268ff-114"> (裝置的名稱通常是從登錄或 SYSTEM.INI 檔案取得。 ) 如果這個成員是常數，它可以是 [ [MCI 裝置類型](mci-device-types.md)] 中所列的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="268ff-114">(The name of the device is typically obtained from the registry or SYSTEM.INI file.) If this member is a constant, it can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="268ff-115">**lpstrElementName**</span><span class="sxs-lookup"><span data-stu-id="268ff-115">**lpstrElementName**</span></span>
</dt> <dd>

<span data-ttu-id="268ff-116">裝置元素名稱通常 (路徑) 。</span><span class="sxs-lookup"><span data-stu-id="268ff-116">Device element name (usually a path).</span></span>

</dd> <dt>

<span data-ttu-id="268ff-117">**lpstrAlias**</span><span class="sxs-lookup"><span data-stu-id="268ff-117">**lpstrAlias**</span></span>
</dt> <dd>

<span data-ttu-id="268ff-118">選用裝置別名。</span><span class="sxs-lookup"><span data-stu-id="268ff-118">Optional device alias.</span></span>

</dd> <dt>

<span data-ttu-id="268ff-119">**dwStyle**</span><span class="sxs-lookup"><span data-stu-id="268ff-119">**dwStyle**</span></span>
</dt> <dd>

<span data-ttu-id="268ff-120">視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="268ff-120">Window style.</span></span>

</dd> <dt>

<span data-ttu-id="268ff-121">**hWndParent**</span><span class="sxs-lookup"><span data-stu-id="268ff-121">**hWndParent**</span></span>
</dt> <dd>

<span data-ttu-id="268ff-122">父視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="268ff-122">Handle to parent window.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="268ff-123">備註</span><span class="sxs-lookup"><span data-stu-id="268ff-123">Remarks</span></span>

<span data-ttu-id="268ff-124">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="268ff-124">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

<span data-ttu-id="268ff-125">如果您不是使用擴充的資料成員，您可以使用 [**mci \_ open \_ PARMS**](mci-open-parms.md) 結構來取代 **mci \_ OVLY \_ open \_ PARMS** 。</span><span class="sxs-lookup"><span data-stu-id="268ff-125">You can use the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure in place of **MCI\_OVLY\_OPEN\_PARMS** if you are not using the extended data members.</span></span>

## <a name="requirements"></a><span data-ttu-id="268ff-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="268ff-126">Requirements</span></span>



| <span data-ttu-id="268ff-127">需求</span><span class="sxs-lookup"><span data-stu-id="268ff-127">Requirement</span></span> | <span data-ttu-id="268ff-128">值</span><span class="sxs-lookup"><span data-stu-id="268ff-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="268ff-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="268ff-129">Minimum supported client</span></span><br/> | <span data-ttu-id="268ff-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="268ff-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="268ff-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="268ff-131">Minimum supported server</span></span><br/> | <span data-ttu-id="268ff-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="268ff-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="268ff-133">標頭</span><span class="sxs-lookup"><span data-stu-id="268ff-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="268ff-134"><dt>Mmsystem。h</dt></span><span class="sxs-lookup"><span data-stu-id="268ff-134"><dt>Mmsystem.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="268ff-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="268ff-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="268ff-136">**Mci**</span><span class="sxs-lookup"><span data-stu-id="268ff-136">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="268ff-137">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="268ff-137">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="268ff-138">**開啟的 MCI \_**</span><span class="sxs-lookup"><span data-stu-id="268ff-138">**MCI\_OPEN**</span></span>](mci-open.md)
</dt> <dt>

[<span data-ttu-id="268ff-139">**MCI \_ 開啟 \_ PARMS**</span><span class="sxs-lookup"><span data-stu-id="268ff-139">**MCI\_OPEN\_PARMS**</span></span>](mci-open-parms.md)
</dt> <dt>

<span data-ttu-id="268ff-140">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="268ff-140">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

