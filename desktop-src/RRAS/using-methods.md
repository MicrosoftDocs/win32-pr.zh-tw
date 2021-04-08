---
title: 使用方法
description: 當用戶端向路由表管理員註冊時，它可以匯出一組方法。 這些方法可供其他用戶端用來取得用戶端特定的資訊。 方法可在路由表管理員的用戶端之間啟用私人通訊。
ms.assetid: 6d984a02-d005-43ad-81c4-968ae9c1a105
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33bd895fbb3f8f54224522786b5794c5c6c57a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932295"
---
# <a name="using-methods"></a>使用方法

當用戶端向路由表管理員註冊時，它可以匯出一組方法。 這些方法可供其他用戶端用來取得用戶端特定的資訊。 方法可在路由表管理員的用戶端之間啟用私人通訊。

用戶端可以取得其他用戶端所匯出的方法清單。 用戶端會呼叫 [**RtmGetEntityMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) 函數，並提供目標用戶端的控制碼。

用戶端匯出的每個方法都是由其方法識別碼唯一識別。 每個用戶端最多可以匯出32方法。 每個方法都會對應到 [**RTM \_ 實體 \_ 匯出 \_ 方法**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method)結構的 **MethodType** 成員中設定的位。 若要叫用多個方法，用戶端應該針對這些方法執行識別碼的邏輯 OR。 當執行通訊協定時，必須指定每個通訊協定的輸入和輸出結構的語法和語義。

> [!Note]  
> 對應到 **MethodType** 成員下半部所設定之位的方法識別碼值 (較低的16位) 是由 Microsoft 所保留。

 

若要叫用第二個用戶端的方法，用戶端會呼叫 [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) 函數。 路由表管理員會仲裁所有呼叫用戶端方法的要求。 路由表管理員在用戶端之間仲裁時，會執行兩個函式：

-   防止第二個用戶端針對正在取消註冊的用戶端叫用方法。
-   在封鎖方法時保留「叫用」要求，並允許在解除封鎖方法時繼續要求。

如果用戶端必須防止其他用戶端執行其方法，則用戶端可以呼叫 [**RtmBlockMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods)。 路由表管理員將不允許對 [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) 進行呼叫，直到用戶端再次解除封鎖其方法為止。

用戶端通常會在對用戶端之間交換的私用資料進行變更時封鎖方法。 封鎖方法是選擇性的動作。 用戶端也可以使用內部鎖定來防止其他用戶端叫用方法。

如需示範如何使用這些函數的範例程式碼，請參閱 [取得和呼叫用戶端的匯出方法](obtain-and-call-the-exported-methods-for-a-client.md)。

 

 




