---
title: 選擇通訊協定順序
description: 選擇通訊協定順序的最佳作法牽涉到使用 ncacn \_ ip \_ tcp 與 ncalrpc，而不是 ncacn \_ np、ncacn \_ spx 和 ncadg \_ \。
ms.assetid: 4b81b534-f001-4522-bf63-044bf5f414f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 732e00d46f1b471870447e228935a794db8d5dc5aa6486e3296b9936cd1be7cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932221"
---
# <a name="choosing-a-protocol-sequence"></a>選擇通訊協定順序

**最佳做法：** 進行遠端呼叫時，請使用 [**ncacn 的 \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp) 。 使用 [**ncalrpc**](/windows/desktop/Midl/ncalrpc) 進行本機呼叫。 請勿使用 [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np)、 [**ncacn \_ spx**](/windows/desktop/Midl/ncacn-spx)或任何 **ncadg \_ \*** 通訊協定序列; 它們的效率較低，且功能較差。

 

 