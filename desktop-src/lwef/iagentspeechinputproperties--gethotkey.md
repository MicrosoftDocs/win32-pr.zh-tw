---
title: IAgentSpeechInputProperties GetHotKey
description: IAgentSpeechInputProperties GetHotKey
ms.assetid: b93e5b46-b8f8-4ca4-8417-7626b97d8928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e672b26f97cfbe92bc71d0ceab165e100c3ecf92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020713"
---
# <a name="iagentspeechinputpropertiesgethotkey"></a><span data-ttu-id="30255-103">IAgentSpeechInputProperties::GetHotKey</span><span class="sxs-lookup"><span data-stu-id="30255-103">IAgentSpeechInputProperties::GetHotKey</span></span>

<span data-ttu-id="30255-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="30255-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHotKey(
BSTR * pbszHotCharKey  // address of variable for listening key 
);                        
```

<span data-ttu-id="30255-105">抓取語音輸入接聽按鍵的目前鍵盤指派。</span><span class="sxs-lookup"><span data-stu-id="30255-105">Retrieves the current keyboard assignment for the speech input Listening key.</span></span>

-   <span data-ttu-id="30255-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="30255-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="30255-107"><span id="pbszHotCharKey"></span><span id="pbszhotcharkey"></span><span id="PBSZHOTCHARKEY"></span>*pbszHotCharKey*</span><span class="sxs-lookup"><span data-stu-id="30255-107"><span id="pbszHotCharKey"></span><span id="pbszhotcharkey"></span><span id="PBSZHOTCHARKEY"></span>*pbszHotCharKey*</span></span>
</dt> <dd>

<span data-ttu-id="30255-108">接收目前用來開啟語音輸入音訊頻道之熱鍵設定的 BSTR 位址。</span><span class="sxs-lookup"><span data-stu-id="30255-108">Address of a BSTR that receives the current hotkey setting used to open the audio channel for speech input.</span></span>

</dd> </dl>

<span data-ttu-id="30255-109">如果 [**GetEnabled**](iagentspeechinputproperties--getenabled.md) 傳回 **False**，則查詢此設定會引發錯誤。</span><span class="sxs-lookup"><span data-stu-id="30255-109">If [**GetEnabled**](iagentspeechinputproperties--getenabled.md) returns **False**, querying this setting raises an error.</span></span>

## <a name="see-also"></a><span data-ttu-id="30255-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30255-110">See Also</span></span>

[<span data-ttu-id="30255-111">**IAgentSpeechInputProperties：： GetEnabled**</span><span class="sxs-lookup"><span data-stu-id="30255-111">**IAgentSpeechInputProperties::GetEnabled**</span></span>](iagentspeechinputproperties--getenabled.md)


 

 




