---
title: 'MCI_SYSINFO 命令 (Mmsystem .h) '
description: MCI \_ SYSINFO 命令會捕獲 mci 裝置的相關資訊。
ms.assetid: 605efd25-8849-42aa-99fd-b36b6fd2c7b7
keywords:
- MCI_SYSINFO 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SYSINFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e722625449893771726a83738c3b0d7bc8bc523c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934485"
---
# <a name="mci_sysinfo-command"></a><span data-ttu-id="4e289-104">MCI \_ SYSINFO 命令</span><span class="sxs-lookup"><span data-stu-id="4e289-104">MCI\_SYSINFO command</span></span>

<span data-ttu-id="4e289-105">MCI \_ SYSINFO 命令會捕獲 mci 裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4e289-105">The MCI\_SYSINFO command retrieves information about MCI devices.</span></span> <span data-ttu-id="4e289-106">MCI 直接支援此命令，而不是將它傳遞至裝置。</span><span class="sxs-lookup"><span data-stu-id="4e289-106">MCI supports this command directly rather than passing it to the device.</span></span> <span data-ttu-id="4e289-107">任何 MCI 應用程式都可以使用此命令。</span><span class="sxs-lookup"><span data-stu-id="4e289-107">Any MCI application can use this command.</span></span> <span data-ttu-id="4e289-108">在由 *lpSysInfo* 所識別之結構的 **lpstrReturn** 成員所指向的應用程式提供的緩衝區中，會傳回字串資訊。</span><span class="sxs-lookup"><span data-stu-id="4e289-108">String information is returned in the application-supplied buffer pointed to by the **lpstrReturn** member of the structure identified by *lpSysInfo*.</span></span> <span data-ttu-id="4e289-109">數值資訊會以 **DWORD** 值的形式傳回，放在應用程式提供的緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="4e289-109">Numeric information is returned as a **DWORD** value placed in the application-supplied buffer.</span></span> <span data-ttu-id="4e289-110">**DwRetSize** 成員指定緩衝區長度。</span><span class="sxs-lookup"><span data-stu-id="4e289-110">The **dwRetSize** member specifies the buffer length.</span></span>

<span data-ttu-id="4e289-111">若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="4e289-111">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SYSINFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SYSINFO_PARMS) lpSysInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4e289-112">參數</span><span class="sxs-lookup"><span data-stu-id="4e289-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e289-113"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="4e289-113"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="4e289-114">要接收命令訊息之 MCI 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="4e289-114">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="4e289-115"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="4e289-115"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="4e289-116">下列一或多個標準和命令特定的旗標：</span><span class="sxs-lookup"><span data-stu-id="4e289-116">One or more of the following standard and command-specific flags:</span></span>

</dd> <dt>

<span data-ttu-id="4e289-117"><span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>MCI \_ SYSINFO \_ INSTALLNAME</span><span class="sxs-lookup"><span data-stu-id="4e289-117"><span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>MCI\_SYSINFO\_INSTALLNAME</span></span>
</dt> <dd>

<span data-ttu-id="4e289-118">取得登錄中列出的名稱 (或用來安裝裝置的 SYSTEM.INI 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="4e289-118">Obtains the name (listed in the registry or the SYSTEM.INI file) used to install the device.</span></span>

</dd> <dt>

<span data-ttu-id="4e289-119"><span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>MCI \_ SYSINFO \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="4e289-119"><span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>MCI\_SYSINFO\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="4e289-120">取得與 **lpSysInfo** 所識別之結構的 **dwNumber** 成員中指定的裝置編號對應的裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="4e289-120">Obtains a device name corresponding to the device number specified in the **dwNumber** member of the structure identified by **lpSysInfo**.</span></span> <span data-ttu-id="4e289-121">如果 \_ \_ 已設定 mci SYSINFO 開啟旗標，mci 會傳回開啟裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e289-121">If the MCI\_SYSINFO\_OPEN flag is set, MCI returns the names of open devices.</span></span>

</dd> <dt>

<span data-ttu-id="4e289-122"><span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>MCI \_ SYSINFO \_ 開啟</span><span class="sxs-lookup"><span data-stu-id="4e289-122"><span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>MCI\_SYSINFO\_OPEN</span></span>
</dt> <dd>

<span data-ttu-id="4e289-123">取得開啟裝置的數量或名稱。</span><span class="sxs-lookup"><span data-stu-id="4e289-123">Obtains the quantity or name of open devices.</span></span>

</dd> <dt>

<span data-ttu-id="4e289-124"><span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>MCI \_ SYSINFO \_ 數量</span><span class="sxs-lookup"><span data-stu-id="4e289-124"><span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>MCI\_SYSINFO\_QUANTITY</span></span>
</dt> <dd>

<span data-ttu-id="4e289-125">取得登錄或 SYSTEM.INI 檔案的 mci 區段中所列指定類型的裝置數目 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="4e289-125">Obtains the number of devices of the specified type that are listed in the registry or the \[mci\] section of the SYSTEM.INI file.</span></span> <span data-ttu-id="4e289-126">如果 \_ \_ 已設定 MCI SYSINFO 開啟旗標，則會傳回開啟的裝置數目。</span><span class="sxs-lookup"><span data-stu-id="4e289-126">If the MCI\_SYSINFO\_OPEN flag is set, the number of open devices is returned.</span></span>

</dd> <dt>

<span data-ttu-id="4e289-127"><span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*lpSysInfo*</span><span class="sxs-lookup"><span data-stu-id="4e289-127"><span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*lpSysInfo*</span></span>
</dt> <dd>

<span data-ttu-id="4e289-128">[**MCI \_ SYSINFO \_ PARMS**](mci-sysinfo-parms.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4e289-128">Pointer to an [**MCI\_SYSINFO\_PARMS**](mci-sysinfo-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e289-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="4e289-129">Return Value</span></span>

<span data-ttu-id="4e289-130">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="4e289-130">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e289-131">備註</span><span class="sxs-lookup"><span data-stu-id="4e289-131">Remarks</span></span>

<span data-ttu-id="4e289-132">*LpSysInfo* 所識別之結構的 **wDeviceType** 成員是用來指出查詢的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="4e289-132">The **wDeviceType** member of the structure identified by *lpSysInfo* is used to indicate the device type of the query.</span></span> <span data-ttu-id="4e289-133">如果 *wDeviceID* 參數設定為 MCI \_ 所有 \_ 裝置 \_ 識別碼，則會覆寫 **wDeviceType** 的值。</span><span class="sxs-lookup"><span data-stu-id="4e289-133">If the *wDeviceID* parameter is set to MCI\_ALL\_DEVICE\_ID, it overrides the value of **wDeviceType**.</span></span> <span data-ttu-id="4e289-134">如需裝置類型的清單，請參閱 [MCI 裝置類型](mci-device-types.md)。</span><span class="sxs-lookup"><span data-stu-id="4e289-134">For a list of device types, see [MCI Device Types](mci-device-types.md).</span></span>

<span data-ttu-id="4e289-135">整數傳回值是由 *lpSysInfo* 所識別之結構的 **lpstrReturn** 成員所指向之緩衝區中傳回的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="4e289-135">Integer return values are **DWORD** values returned in the buffer pointed to by the **lpstrReturn** member of the structure identified by *lpSysInfo*.</span></span>

<span data-ttu-id="4e289-136">字串傳回值是以 null 終止的字串，在由 *lpSysInfo* 所識別之結構的 **lpstrReturn** 成員所指向的緩衝區中傳回。</span><span class="sxs-lookup"><span data-stu-id="4e289-136">String return values are null-terminated strings returned in the buffer pointed to by the **lpstrReturn** member of the structure identified by *lpSysInfo*.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e289-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e289-137">Requirements</span></span>



| <span data-ttu-id="4e289-138">需求</span><span class="sxs-lookup"><span data-stu-id="4e289-138">Requirement</span></span> | <span data-ttu-id="4e289-139">值</span><span class="sxs-lookup"><span data-stu-id="4e289-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e289-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4e289-140">Minimum supported client</span></span><br/> | <span data-ttu-id="4e289-141">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e289-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4e289-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4e289-142">Minimum supported server</span></span><br/> | <span data-ttu-id="4e289-143">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e289-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4e289-144">標頭</span><span class="sxs-lookup"><span data-stu-id="4e289-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e289-145"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="4e289-145"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e289-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e289-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e289-147">Mci</span><span class="sxs-lookup"><span data-stu-id="4e289-147">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4e289-148">MCI 命令</span><span class="sxs-lookup"><span data-stu-id="4e289-148">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

