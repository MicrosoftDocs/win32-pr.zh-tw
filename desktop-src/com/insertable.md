---
title: '插入 (CLSID 金鑰) '
description: 指出當 COM 容器應用程式使用時，這個類別的物件應該出現在 [插入物件] 對話方塊清單方塊中。
ms.assetid: 908cbfc4-ebf8-454e-b2e5-34449de60e7f
keywords:
- 插入登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da4892fb13de5954dabe7c55759900dba32f854
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024482"
---
# <a name="insertable-clsid-key"></a><span data-ttu-id="e86bc-104">插入 (CLSID 金鑰) </span><span class="sxs-lookup"><span data-stu-id="e86bc-104">Insertable (CLSID Key)</span></span>

<span data-ttu-id="e86bc-105">指出當 COM 容器應用程式使用時，這個類別的物件應該出現在 [ **插入物件** ] 對話方塊清單方塊中。</span><span class="sxs-lookup"><span data-stu-id="e86bc-105">Indicates that objects of this class should appear in the **Insert Object** dialog box list box when used by COM container applications.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="e86bc-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="e86bc-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Insertable
```

## <a name="remarks"></a><span data-ttu-id="e86bc-107">備註</span><span class="sxs-lookup"><span data-stu-id="e86bc-107">Remarks</span></span>

<span data-ttu-id="e86bc-108">此索引鍵是32位 COM 應用程式的必要專案，其物件可以插入現有的16位應用程式。</span><span class="sxs-lookup"><span data-stu-id="e86bc-108">This key is a required entry for 32-bit COM applications whose objects can be inserted into existing 16-bit applications.</span></span> <span data-ttu-id="e86bc-109">現有的16位應用程式會在登錄中查看此機碼，這會通知應用程式伺服器支援內嵌。</span><span class="sxs-lookup"><span data-stu-id="e86bc-109">Existing 16-bit applications look in the registry for this key, which informs the application that the server supports embeddings.</span></span> <span data-ttu-id="e86bc-110">如果可 **插入** 的機碼存在，16位應用程式也可能會嘗試確認伺服器是否存在於電腦上。</span><span class="sxs-lookup"><span data-stu-id="e86bc-110">If the **Insertable** key exists, 16-bit applications may also attempt to verify that the server exists on the machine.</span></span> <span data-ttu-id="e86bc-111">16位應用程式通常會從類別取出 [**LocalServer**](localserver.md) 索引鍵的值，並檢查它是否為系統上的有效檔案。</span><span class="sxs-lookup"><span data-stu-id="e86bc-111">16-bit applications typically retrieve the value of the [**LocalServer**](localserver.md) key from the class and check to see whether it is a valid file on the system.</span></span> <span data-ttu-id="e86bc-112">因此，若要讓32位應用程式可供16位應用程式插入，32位應用程式除了註冊 [**LocalServer32**](localserver32.md)，還應該註冊 **LocalServer** 子機碼。</span><span class="sxs-lookup"><span data-stu-id="e86bc-112">Therefore, for a 32-bit application to be insertable by a 16-bit application, the 32-bit application should register the **LocalServer** subkey in addition to registering [**LocalServer32**](localserver32.md).</span></span>

<span data-ttu-id="e86bc-113">與控制項搭配使用時，此專案表示物件只能做為就地内嵌物件，且沒有特殊的控制項功能。</span><span class="sxs-lookup"><span data-stu-id="e86bc-113">Used with controls, this entry indicates that an object can act only as an in-place embedded object with no special control features.</span></span> <span data-ttu-id="e86bc-114">具有此索引鍵的物件會顯示在其容器的 [ **插入物件** ] 對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="e86bc-114">Objects that have this key appear in the **Insert Object** dialog box for their container.</span></span> <span data-ttu-id="e86bc-115">搭配控制項使用時，此專案也會指出控制項已使用非控制項容器進行測試。</span><span class="sxs-lookup"><span data-stu-id="e86bc-115">When used with controls, this entry also indicates the control has been tested with non-control containers.</span></span> <span data-ttu-id="e86bc-116">這個專案也是選擇性的，當控制項不是設計來使用不了解控制項的舊版容器時，可以省略此專案。</span><span class="sxs-lookup"><span data-stu-id="e86bc-116">This entry is also optional and can be omitted when a control is not designed to work with older containers that do not understand controls.</span></span>

> [!Note]  
> <span data-ttu-id="e86bc-117">此索引鍵不存在於內部類別，例如「標記」類別。</span><span class="sxs-lookup"><span data-stu-id="e86bc-117">This key is not present for internal classes like the moniker classes.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e86bc-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="e86bc-118">Related topics</span></span>

<dl> <dt>

[**<ProgID>**](-progid--key.md)
</dt> </dl>

 

 




