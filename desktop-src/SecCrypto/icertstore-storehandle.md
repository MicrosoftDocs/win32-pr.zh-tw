---
description: 設定或抓取證書存儲的 HCERTSTORE 控制碼。
ms.assetid: 3ff8b4c7-4a9a-4cc1-b0ea-da442ebce157
title: ICertStore：： StoreHandle 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreHandle
- ICertStore.get_StoreHandle
- ICertStore.put_StoreHandle
- CertStore.StoreHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 86f57159a2fdd444f22593ec66fa99510a5260b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977540"
---
# <a name="icertstorestorehandle-property"></a><span data-ttu-id="73136-103">ICertStore：： StoreHandle 屬性</span><span class="sxs-lookup"><span data-stu-id="73136-103">ICertStore::StoreHandle property</span></span>

<span data-ttu-id="73136-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。\]</span><span class="sxs-lookup"><span data-stu-id="73136-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="73136-105">**StoreHandle** 屬性會設定或抓取證書存儲的 HCERTSTORE 控制碼。</span><span class="sxs-lookup"><span data-stu-id="73136-105">The **StoreHandle** property sets or retrieves the HCERTSTORE handle of a certificate store.</span></span>

<span data-ttu-id="73136-106">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="73136-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="73136-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="73136-107">Syntax</span></span>


```VB
CertStore.StoreHandle As Long
```



## <a name="property-value"></a><span data-ttu-id="73136-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="73136-108">Property value</span></span>

<span data-ttu-id="73136-109">憑證存放區的 HCERTSTORE 控制碼。</span><span class="sxs-lookup"><span data-stu-id="73136-109">The HCERTSTORE handle of the certificate store.</span></span>

## <a name="error-codes"></a><span data-ttu-id="73136-110">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="73136-110">Error codes</span></span>

<span data-ttu-id="73136-111">如果屬性存取方法 **put \_ StoreHandle** 並 **讓 \_ StoreHandle** 成功，則會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="73136-111">If the property access methods **put\_StoreHandle** and **get\_StoreHandle** succeed, they return S\_OK.</span></span>

<span data-ttu-id="73136-112">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="73136-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="73136-113">備註</span><span class="sxs-lookup"><span data-stu-id="73136-113">Remarks</span></span>

<span data-ttu-id="73136-114">您必須呼叫 [**CloseHandle**](icertstore-closehandle.md) 方法或 [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) 函數來釋放內容。</span><span class="sxs-lookup"><span data-stu-id="73136-114">You must call either the [**CloseHandle**](icertstore-closehandle.md) method or the [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) function to free the context.</span></span>

<span data-ttu-id="73136-115">如果您設定 **StoreHandle** 屬性，則會重設整個 [**存放區**](store.md) 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="73136-115">If you set the **StoreHandle** property, the state of the entire [**Store**](store.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="73136-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="73136-116">Requirements</span></span>



| <span data-ttu-id="73136-117">需求</span><span class="sxs-lookup"><span data-stu-id="73136-117">Requirement</span></span> | <span data-ttu-id="73136-118">值</span><span class="sxs-lookup"><span data-stu-id="73136-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73136-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="73136-119">Redistributable</span></span><br/> | <span data-ttu-id="73136-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="73136-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="73136-121">DLL</span><span class="sxs-lookup"><span data-stu-id="73136-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="73136-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73136-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73136-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73136-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73136-124">**ICertStore**</span><span class="sxs-lookup"><span data-stu-id="73136-124">**ICertStore**</span></span>](icertstore.md)
</dt> </dl>

 

 




