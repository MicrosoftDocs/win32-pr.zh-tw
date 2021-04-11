---
description: 包含電池查詢資訊。
ms.assetid: ef5466fe-7de8-48cd-ad48-5774d7a4bb46
title: 'BATTERY_QUERY_INFORMATION 結構 (Poclass .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_QUERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 511980dd4307077b8b160550c661a15a5714b96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849274"
---
# <a name="battery_query_information-structure"></a><span data-ttu-id="f995e-103">電池 \_ 查詢 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="f995e-103">BATTERY\_QUERY\_INFORMATION structure</span></span>

<span data-ttu-id="f995e-104">包含電池查詢資訊。</span><span class="sxs-lookup"><span data-stu-id="f995e-104">Contains battery query information.</span></span> <span data-ttu-id="f995e-105">此結構會與 [**IOCTL \_ 電池 \_ 查詢 \_ 資訊**](ioctl-battery-query-information.md) 控制項程式碼搭配使用，以指定要傳回的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="f995e-105">This structure is used with the [**IOCTL\_BATTERY\_QUERY\_INFORMATION**](ioctl-battery-query-information.md) control code to specify the type of information to return.</span></span>

## <a name="syntax"></a><span data-ttu-id="f995e-106">語法</span><span class="sxs-lookup"><span data-stu-id="f995e-106">Syntax</span></span>


```C++
typedef struct _BATTERY_QUERY_INFORMATION {
  ULONG                           BatteryTag;
  BATTERY_QUERY_INFORMATION_LEVEL InformationLevel;
  LONG                            AtRate;
} BATTERY_QUERY_INFORMATION, *PBATTERY_QUERY_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="f995e-107">成員</span><span class="sxs-lookup"><span data-stu-id="f995e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f995e-108">**BatteryTag**</span><span class="sxs-lookup"><span data-stu-id="f995e-108">**BatteryTag**</span></span>
</dt> <dd>

<span data-ttu-id="f995e-109">電池目前的電池標記。</span><span class="sxs-lookup"><span data-stu-id="f995e-109">The current battery tag for the battery.</span></span> <span data-ttu-id="f995e-110">只會傳回符合標記之電池的資訊。</span><span class="sxs-lookup"><span data-stu-id="f995e-110">Only information for a battery matching the tag can be returned.</span></span> <span data-ttu-id="f995e-111">每當此值不符合電池的目前標記時，就會完成 IOCTL 要求，並 \_ \_ 找不到錯誤檔案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f995e-111">Whenever this value does not match the battery's current tag, the IOCTL request will be completed with ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="f995e-112">這會向呼叫者指出與標記相關聯的電池已存在。</span><span class="sxs-lookup"><span data-stu-id="f995e-112">This indicates to the caller that the battery associated with the tag longer exists.</span></span> <span data-ttu-id="f995e-113">呼叫者可以選擇使用 [**IOCTL \_ 電池 \_ 查詢 \_ 標記**](ioctl-battery-query-tag.md) 作業來判斷新安裝的電池標記（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="f995e-113">The caller may opt to use the [**IOCTL\_BATTERY\_QUERY\_TAG**](ioctl-battery-query-tag.md) operation to determine the tag of the newly installed battery, if one exists.</span></span> <span data-ttu-id="f995e-114"> (查看 [電池標記](battery-information.md) 以取得詳細資訊。 ) </span><span class="sxs-lookup"><span data-stu-id="f995e-114">(See [Battery Tags](battery-information.md) for more information.)</span></span>

<span data-ttu-id="f995e-115">發出查詢資訊要求時，會驗證此值。</span><span class="sxs-lookup"><span data-stu-id="f995e-115">When a query information request is made, this value is verified.</span></span> <span data-ttu-id="f995e-116">此外，如果此值變更時，要求仍在進行中，則會中止要求，並出現「找不到錯誤檔案」的狀態 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="f995e-116">In addition, if the request is in progress while this value changes, the request is aborted with the status of ERROR\_FILE\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="f995e-117">**InformationLevel**</span><span class="sxs-lookup"><span data-stu-id="f995e-117">**InformationLevel**</span></span>
</dt> <dd>

<span data-ttu-id="f995e-118">正在查詢的電池資訊層級。</span><span class="sxs-lookup"><span data-stu-id="f995e-118">The level of the battery information being queried.</span></span> <span data-ttu-id="f995e-119">由 IOCTL 傳回的資料取決於此值。</span><span class="sxs-lookup"><span data-stu-id="f995e-119">The data returned by the IOCTL depends on this value.</span></span> <span data-ttu-id="f995e-120">這個成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f995e-120">This member can be one of the following values.</span></span>



| <span data-ttu-id="f995e-121">值</span><span class="sxs-lookup"><span data-stu-id="f995e-121">Value</span></span>                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="f995e-122">意義</span><span class="sxs-lookup"><span data-stu-id="f995e-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryDeviceName"></span><span id="batterydevicename"></span><span id="BATTERYDEVICENAME"></span><dl> <span data-ttu-id="f995e-123"><dt>**BatteryDeviceName**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f995e-123"><dt>**BatteryDeviceName**</dt> <dt>4</dt></span></span> </dl>                                                 | <span data-ttu-id="f995e-124">以 Null 終止的 Unicode 字串，其中包含電池的名稱。</span><span class="sxs-lookup"><span data-stu-id="f995e-124">Null-terminated Unicode string that contains the battery's name.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="BatteryEstimatedTime"></span><span id="batteryestimatedtime"></span><span id="BATTERYESTIMATEDTIME"></span><dl> <span data-ttu-id="f995e-125"><dt>**BatteryEstimatedTime**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f995e-125"><dt>**BatteryEstimatedTime**</dt> <dt>3</dt></span></span> </dl>                                     | <span data-ttu-id="f995e-126">指定預估電池執行時間（以秒為單位）的 **ULONG** 。</span><span class="sxs-lookup"><span data-stu-id="f995e-126">A **ULONG** that specifies the estimated battery run time, in seconds.</span></span> <span data-ttu-id="f995e-127">如果 **電池 \_ 查詢 \_ 資訊** 結構的 **AtRate** 成員中提供的清空率為零，則此計算是以目前的清空率為基礎。</span><span class="sxs-lookup"><span data-stu-id="f995e-127">If the rate of drain provided in the **AtRate** member of the **BATTERY\_QUERY\_INFORMATION** structure is zero, this calculation is based on the present rate of drain.</span></span> <span data-ttu-id="f995e-128">如果 **AtRate** 為非零值，則傳回的時間會是指定速率的預期執行時間。</span><span class="sxs-lookup"><span data-stu-id="f995e-128">If **AtRate** is nonzero, the time returned is the expected run time for the given rate.</span></span> <span data-ttu-id="f995e-129">如果預估的時間不明 (例如，電池未放電，且指定的 **AtRate** 為零) ，則傳回值為電池 \_ 未知 \_ 時間。</span><span class="sxs-lookup"><span data-stu-id="f995e-129">If the estimated time is unknown (for example, the battery is not discharging and the **AtRate** specified was zero), the return value is BATTERY\_UNKNOWN\_TIME.</span></span> <span data-ttu-id="f995e-130">請注意，在某些電池系統上，此值不太精確，而且可能會因為目前的電源使用量而異，可能會受到磁片活動和其他因素所影響。</span><span class="sxs-lookup"><span data-stu-id="f995e-130">Note that this value is not very accurate on some battery systems, and may vary widely depending on present power usage, which could be affected by disk activity and other factors.</span></span> <span data-ttu-id="f995e-131">此值的變更不會有任何通知機制。</span><span class="sxs-lookup"><span data-stu-id="f995e-131">There is no notification mechanism for changes in this value.</span></span><br/> |
| <span id="BatteryGranularityInformation"></span><span id="batterygranularityinformation"></span><span id="BATTERYGRANULARITYINFORMATION"></span><dl> <span data-ttu-id="f995e-132"><dt>**BatteryGranularityInformation**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f995e-132"><dt>**BatteryGranularityInformation**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="f995e-133">[**電池 \_ 報告 \_ 規模**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)結構的陣列，不超過四個專案。</span><span class="sxs-lookup"><span data-stu-id="f995e-133">An array of [**BATTERY\_REPORTING\_SCALE**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) structures, never more than four entries.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="BatteryInformation"></span><span id="batteryinformation"></span><span id="BATTERYINFORMATION"></span><dl> <span data-ttu-id="f995e-134"><dt>**BatteryInformation**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f995e-134"><dt>**BatteryInformation**</dt> <dt>0</dt></span></span> </dl>                                             | <span data-ttu-id="f995e-135">[**電池 \_ 資訊**](battery-information-str.md)結構。</span><span class="sxs-lookup"><span data-stu-id="f995e-135">A [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BatteryManufactureDate"></span><span id="batterymanufacturedate"></span><span id="BATTERYMANUFACTUREDATE"></span><dl> <span data-ttu-id="f995e-136"><dt>**BatteryManufactureDate**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="f995e-136"><dt>**BatteryManufactureDate**</dt> <dt>5</dt></span></span> </dl>                             | <span data-ttu-id="f995e-137">[**電池 \_ 製造 \_ 日期**](battery-manufacture-date-str.md)結構。</span><span class="sxs-lookup"><span data-stu-id="f995e-137">A [**BATTERY\_MANUFACTURE\_DATE**](battery-manufacture-date-str.md) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="BatteryManufactureName"></span><span id="batterymanufacturename"></span><span id="BATTERYMANUFACTURENAME"></span><dl> <span data-ttu-id="f995e-138"><dt>**BatteryManufactureName**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f995e-138"><dt>**BatteryManufactureName**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="f995e-139">以 Null 結束的 Unicode 字串，指定電池的製造商名稱。</span><span class="sxs-lookup"><span data-stu-id="f995e-139">Null-terminated Unicode string that specifies the name of the manufacturer of the battery.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatterySerialNumber"></span><span id="batteryserialnumber"></span><span id="BATTERYSERIALNUMBER"></span><dl> <span data-ttu-id="f995e-140"><dt>**BatterySerialNumber**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="f995e-140"><dt>**BatterySerialNumber**</dt> <dt>8</dt></span></span> </dl>                                         | <span data-ttu-id="f995e-141">以 Null 結束的 Unicode 字串，指定電池的序號。</span><span class="sxs-lookup"><span data-stu-id="f995e-141">Null-terminated Unicode string that specifies the battery's serial number.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatteryTemperature"></span><span id="batterytemperature"></span><span id="BATTERYTEMPERATURE"></span><dl> <span data-ttu-id="f995e-142"><dt>**BatteryTemperature**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f995e-142"><dt>**BatteryTemperature**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="f995e-143">指定電池目前溫度的 **ULONG** ，以10ths 角度的角度。</span><span class="sxs-lookup"><span data-stu-id="f995e-143">A **ULONG** that specifies the battery's current temperature, in 10ths of a degree Kelvin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="BatteryUniqueID"></span><span id="batteryuniqueid"></span><span id="BATTERYUNIQUEID"></span><dl> <span data-ttu-id="f995e-144"><dt>**BatteryUniqueID**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="f995e-144"><dt>**BatteryUniqueID**</dt> <dt>7</dt></span></span> </dl>                                                         | <span data-ttu-id="f995e-145">以 Null 結束的 Unicode 字串，可唯一識別電池。</span><span class="sxs-lookup"><span data-stu-id="f995e-145">Null-terminated Unicode string that uniquely identifies the battery.</span></span> <span data-ttu-id="f995e-146">這個值可以用來追蹤特定電池。</span><span class="sxs-lookup"><span data-stu-id="f995e-146">This value can be used to track a specific battery.</span></span> <span data-ttu-id="f995e-147">在智慧電池的情況下，此識別碼會是製造商名稱、裝置名稱、製造日期，以及序號可列印標記法的串連。</span><span class="sxs-lookup"><span data-stu-id="f995e-147">In the case of smart batteries, this ID would be the concatenation of the manufacturer's name, device name, date of manufacture, and a printable representation of the serial number.</span></span> <br/> <span data-ttu-id="f995e-148">此值不適合顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="f995e-148">This value is not intended to be displayed to the user.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="f995e-149">**AtRate**</span><span class="sxs-lookup"><span data-stu-id="f995e-149">**AtRate**</span></span>
</dt> <dd>

<span data-ttu-id="f995e-150">只有在 **InformationLevel** 為 BatteryEstimatedTime 時，才會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="f995e-150">This member is used only if **InformationLevel** is BatteryEstimatedTime.</span></span>

<span data-ttu-id="f995e-151">如果這個成員為非零值，則會用來計算時間，直到電池放電以 BatteryEstimatedTime 個別電池的速率。</span><span class="sxs-lookup"><span data-stu-id="f995e-151">If this member is nonzero, it is a rate of drain that will be used to calculate the time until the battery is discharged for the BatteryEstimatedTime of an individual battery.</span></span> <span data-ttu-id="f995e-152">它必須在 mW 中指定，而且必須是負數值，以代表電池放電率。</span><span class="sxs-lookup"><span data-stu-id="f995e-152">It must be specified in mW, and must be a negative value to represent a battery discharge rate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f995e-153">備註</span><span class="sxs-lookup"><span data-stu-id="f995e-153">Remarks</span></span>

<span data-ttu-id="f995e-154">某些電池的相關資訊是選擇性的，或可能對某些電池沒有意義。</span><span class="sxs-lookup"><span data-stu-id="f995e-154">Some information about batteries is optional or may be meaningless for some batteries.</span></span> <span data-ttu-id="f995e-155">如果目前的電池無法使用所要求的特定資料類型，則會傳回錯誤不正確函式 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="f995e-155">If the particular type of data requested is not available for the current battery, then ERROR\_INVALID\_FUNCTION is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="f995e-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="f995e-156">Requirements</span></span>



| <span data-ttu-id="f995e-157">需求</span><span class="sxs-lookup"><span data-stu-id="f995e-157">Requirement</span></span> | <span data-ttu-id="f995e-158">值</span><span class="sxs-lookup"><span data-stu-id="f995e-158">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f995e-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f995e-159">Minimum supported client</span></span><br/> | <span data-ttu-id="f995e-160">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f995e-160">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="f995e-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f995e-161">Minimum supported server</span></span><br/> | <span data-ttu-id="f995e-162">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f995e-162">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="f995e-163">標頭</span><span class="sxs-lookup"><span data-stu-id="f995e-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="f995e-164"><dt>Poclass .h;</dt><dt>Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP 上的 Batclass .h</dt></span><span class="sxs-lookup"><span data-stu-id="f995e-164"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f995e-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f995e-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f995e-166">**電池 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f995e-166">**BATTERY\_INFORMATION**</span></span>](battery-information-str.md)
</dt> <dt>

[<span data-ttu-id="f995e-167">**電池 \_ 製造 \_ 日期**</span><span class="sxs-lookup"><span data-stu-id="f995e-167">**BATTERY\_MANUFACTURE\_DATE**</span></span>](battery-manufacture-date-str.md)
</dt> <dt>

[<span data-ttu-id="f995e-168">**電池 \_ 報告 \_ 規模**</span><span class="sxs-lookup"><span data-stu-id="f995e-168">**BATTERY\_REPORTING\_SCALE**</span></span>](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[<span data-ttu-id="f995e-169">**IOCTL \_ 電池 \_ 查詢 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f995e-169">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> <dt>

[<span data-ttu-id="f995e-170">**IOCTL \_ 電池 \_ 查詢 \_ 標記**</span><span class="sxs-lookup"><span data-stu-id="f995e-170">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> </dl>

 

 




