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
# <a name="insertable-clsid-key"></a>插入 (CLSID 金鑰) 

指出當 COM 容器應用程式使用時，這個類別的物件應該出現在 [ **插入物件** ] 對話方塊清單方塊中。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Insertable
```

## <a name="remarks"></a>備註

此索引鍵是32位 COM 應用程式的必要專案，其物件可以插入現有的16位應用程式。 現有的16位應用程式會在登錄中查看此機碼，這會通知應用程式伺服器支援內嵌。 如果可 **插入** 的機碼存在，16位應用程式也可能會嘗試確認伺服器是否存在於電腦上。 16位應用程式通常會從類別取出 [**LocalServer**](localserver.md) 索引鍵的值，並檢查它是否為系統上的有效檔案。 因此，若要讓32位應用程式可供16位應用程式插入，32位應用程式除了註冊 [**LocalServer32**](localserver32.md)，還應該註冊 **LocalServer** 子機碼。

與控制項搭配使用時，此專案表示物件只能做為就地内嵌物件，且沒有特殊的控制項功能。 具有此索引鍵的物件會顯示在其容器的 [ **插入物件** ] 對話方塊中。 搭配控制項使用時，此專案也會指出控制項已使用非控制項容器進行測試。 這個專案也是選擇性的，當控制項不是設計來使用不了解控制項的舊版容器時，可以省略此專案。

> [!Note]  
> 此索引鍵不存在於內部類別，例如「標記」類別。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**<ProgID>**](-progid--key.md)
</dt> </dl>

 

 




