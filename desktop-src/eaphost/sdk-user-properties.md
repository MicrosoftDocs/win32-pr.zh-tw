---
title: SDK 使用者屬性
description: 瞭解 SDK 使用者屬性。 請參閱 eaphostusercredentials 原生架構實例的範例。
ms.assetid: e8a9656d-48e7-4580-a84d-2b829e7a692f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c8dab154e1ef6c736849720856a23fdfe2e7b3
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104093447"
---
# <a name="sdk-user-properties"></a><span data-ttu-id="3a984-104">SDK 使用者屬性</span><span class="sxs-lookup"><span data-stu-id="3a984-104">SDK User Properties</span></span>

<span data-ttu-id="3a984-105">這個範例是 [eaphostusercredentials](eaphostusercredentialsschema-schema.md) 原生架構的實例。</span><span class="sxs-lookup"><span data-stu-id="3a984-105">This sample is an instance of the [eaphostusercredentials](eaphostusercredentialsschema-schema.md) native schema.</span></span>

``` syntax
  <?xml version="1.0" ?>  
  <EapHostUserCredentials xmlns="https://www.microsoft.com/provisioning/EapHostUserCredentials" 
    xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
    xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodUserCredentials">
    <EapMethod>
      <eapCommon:Type>40</eapCommon:Type> 
      <eapCommon:AuthorId>100</eapCommon:AuthorId> 
    </EapMethod> 
    <Credentials>
      <EapType>40</EapType> 
      <Identity>test</Identity> 
      <Password>test</Password> 
    </Credentials>
  </EapHostUserCredentials>
```

## <a name="related-topics"></a><span data-ttu-id="3a984-106">相關主題</span><span class="sxs-lookup"><span data-stu-id="3a984-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a984-107">使用者屬性</span><span class="sxs-lookup"><span data-stu-id="3a984-107">User Properties</span></span>](user-profiles.md)
</dt> <dt>

[<span data-ttu-id="3a984-108">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="3a984-108">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




