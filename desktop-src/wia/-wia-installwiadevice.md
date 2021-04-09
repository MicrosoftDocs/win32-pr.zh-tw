---
description: InstallWiaDevice 函式會將 Windows 映像取得 (WIA) 裝置安裝為根列舉的裝置。 如果有任何安裝的檔案或 coinstaller 未經過數位簽署且受信任，它可能會彈出安全性警告。
ms.assetid: c7de27f5-5994-4fce-a6ec-6e7cfae2e591
title: 'InstallWiaDevice 函式 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallWiaDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 62060d538b4b51fe22e10df09093f1f7f8c26a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691108"
---
# <a name="installwiadevice-function"></a><span data-ttu-id="224a5-104">InstallWiaDevice 函式</span><span class="sxs-lookup"><span data-stu-id="224a5-104">InstallWiaDevice function</span></span>

<span data-ttu-id="224a5-105">**InstallWiaDevice** 函式會將 Windows 映像取得 (WIA) 裝置安裝為根列舉的裝置。</span><span class="sxs-lookup"><span data-stu-id="224a5-105">The **InstallWiaDevice** function installs a Windows Image Acquisition (WIA) device as root-enumerated device.</span></span> <span data-ttu-id="224a5-106">如果有任何安裝的檔案或 coinstaller 未經過數位簽署且受信任，它可能會彈出安全性警告。</span><span class="sxs-lookup"><span data-stu-id="224a5-106">It may popup a security warning if any installing file or coinstaller is not digitally signed and trusted.</span></span>

## <a name="syntax"></a><span data-ttu-id="224a5-107">語法</span><span class="sxs-lookup"><span data-stu-id="224a5-107">Syntax</span></span>


```C++
DWORD WINAPI InstallWiaDevice(
  _In_ PWIADEVICEINSTALL *pWiaDeviceInstall
);
```



## <a name="parameters"></a><span data-ttu-id="224a5-108">參數</span><span class="sxs-lookup"><span data-stu-id="224a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="224a5-109">*pWiaDeviceInstall* \[在\]</span><span class="sxs-lookup"><span data-stu-id="224a5-109">*pWiaDeviceInstall* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="224a5-110">類型： \**PWIADEVICEINSTALL \** _</span><span class="sxs-lookup"><span data-stu-id="224a5-110">Type: \**PWIADEVICEINSTALL\** _</span></span>

<span data-ttu-id="224a5-111">WIADEVICEINSTALL 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="224a5-111">Pointer to a WIADEVICEINSTALL structure.</span></span> <span data-ttu-id="224a5-112">結構的 _szFriendlyName \* 成員必須設定為實際的裝置 FriendlyName。</span><span class="sxs-lookup"><span data-stu-id="224a5-112">The _szFriendlyName\* member of the structure must be set to the actual device FriendlyName.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="224a5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="224a5-113">Return value</span></span>

<span data-ttu-id="224a5-114">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="224a5-114">Type: **DWORD**</span></span>

<span data-ttu-id="224a5-115">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="224a5-115">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="224a5-116">如果函式失敗，則會傳回 Win32 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="224a5-116">If the function fails, it returns a Win32 error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="224a5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="224a5-117">Requirements</span></span>



| <span data-ttu-id="224a5-118">需求</span><span class="sxs-lookup"><span data-stu-id="224a5-118">Requirement</span></span> | <span data-ttu-id="224a5-119">值</span><span class="sxs-lookup"><span data-stu-id="224a5-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="224a5-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="224a5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="224a5-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="224a5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="224a5-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="224a5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="224a5-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="224a5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="224a5-124">標頭</span><span class="sxs-lookup"><span data-stu-id="224a5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="224a5-125"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="224a5-125"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="224a5-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="224a5-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="224a5-127"><dt>Wiaguid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="224a5-127"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




