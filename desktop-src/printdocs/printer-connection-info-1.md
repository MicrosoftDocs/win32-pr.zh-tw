---
description: 代表印表機連接的相關資訊。
ms.assetid: afac3f91-74eb-46f7-94b4-d37b2b8a32a4
title: 'PRINTER_CONNECTION_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_CONNECTION_INFO_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 04bfb5411a5602248bcd188d07dec8478462fd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693563"
---
# <a name="printer_connection_info_1-structure"></a><span data-ttu-id="c8fe2-103">印表機 \_ 連接 \_ 資訊 \_ 1 結構</span><span class="sxs-lookup"><span data-stu-id="c8fe2-103">PRINTER\_CONNECTION\_INFO\_1 structure</span></span>

<span data-ttu-id="c8fe2-104">代表印表機連接的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c8fe2-104">Represents information about a connection to a printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8fe2-105">語法</span><span class="sxs-lookup"><span data-stu-id="c8fe2-105">Syntax</span></span>


```C++
typedef struct _PRINTER_CONNECTION_INFO_1 {
  DWORD  dwFlags;
  LPTSTR pszDriverName;
} PRINTER_CONNECTION_INFO_1, *PPRINTER_CONNECTION_INFO_1;
```



## <a name="members"></a><span data-ttu-id="c8fe2-106">成員</span><span class="sxs-lookup"><span data-stu-id="c8fe2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c8fe2-107">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="c8fe2-107">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="c8fe2-108">系統會定義下列值：</span><span class="sxs-lookup"><span data-stu-id="c8fe2-108">The following values are defined:</span></span>



| <span data-ttu-id="c8fe2-109">值</span><span class="sxs-lookup"><span data-stu-id="c8fe2-109">Value</span></span>                                      | <span data-ttu-id="c8fe2-110">意義</span><span class="sxs-lookup"><span data-stu-id="c8fe2-110">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8fe2-111">\_ \_ (0x00000020) 的印表機連接不相符</span><span class="sxs-lookup"><span data-stu-id="c8fe2-111">PRINTER\_CONNECTION\_MISMATCH (0x00000020)</span></span> | <span data-ttu-id="c8fe2-112">如果設定此位旗標，則印表機連接不相符。</span><span class="sxs-lookup"><span data-stu-id="c8fe2-112">If this bit-flag is set, the printer connection is mismatched.</span></span> <span data-ttu-id="c8fe2-113">使用者可以提供本機列印驅動程式做為 *pszDriverName* ，並使用它來進行轉譯，而不是使用安裝在使用者所連接之伺服器印表機上的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="c8fe2-113">The user can supply a local print driver as *pszDriverName* and use it to do the rendering instead of using the driver installed on the server printer to which the user is connected.</span></span><br/>                                                                                                                                                                                                                                    |
| <span data-ttu-id="c8fe2-114">印表機 \_ 連線 \_ 沒有 \_ UI (0x00000040) </span><span class="sxs-lookup"><span data-stu-id="c8fe2-114">PRINTER\_CONNECTION\_NO\_UI (0x00000040)</span></span>   | <span data-ttu-id="c8fe2-115">如果設定此位旗標，則此呼叫無法顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c8fe2-115">If this bit-flag is set then this call cannot display a dialog box.</span></span> <span data-ttu-id="c8fe2-116">如果必須顯示對話方塊以從伺服器安裝印表機驅動程式，且已設定此位旗標，則不會安裝印表機驅動程式，也不會新增印表機連線，而且呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="c8fe2-116">If a dialog box must be displayed to install a printer driver from the server and this bit-flag is set, the printer driver will not be installed, the printer connection will not be added, and the call will fail.</span></span><br/> <span data-ttu-id="c8fe2-117">**Windows 7：** 在 Windows 7 和更新版本的 Windows 中，如果已設定這個旗標，而且使用者是在提高許可權的模式下執行，就不會顯示 [ **您信任此印表機嗎？** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c8fe2-117">**Windows 7:** In Windows 7 and later versions of Windows, if this flag is set and the user is running in elevated mode, the **Do you trust this printer?** dialog will not be shown.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c8fe2-118">**pszDriverName**</span><span class="sxs-lookup"><span data-stu-id="c8fe2-118">**pszDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="c8fe2-119">驅動程式名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="c8fe2-119">A pointer to the name of the driver.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8fe2-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8fe2-120">Requirements</span></span>



| <span data-ttu-id="c8fe2-121">需求</span><span class="sxs-lookup"><span data-stu-id="c8fe2-121">Requirement</span></span> | <span data-ttu-id="c8fe2-122">值</span><span class="sxs-lookup"><span data-stu-id="c8fe2-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8fe2-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8fe2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c8fe2-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8fe2-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c8fe2-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8fe2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c8fe2-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8fe2-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c8fe2-127">標頭</span><span class="sxs-lookup"><span data-stu-id="c8fe2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8fe2-128"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c8fe2-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8fe2-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8fe2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8fe2-130">列印</span><span class="sxs-lookup"><span data-stu-id="c8fe2-130">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c8fe2-131">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="c8fe2-131">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




