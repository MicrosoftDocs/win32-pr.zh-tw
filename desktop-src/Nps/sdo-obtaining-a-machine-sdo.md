---
title: 取得電腦 SDO
description: 使用 SDO API 的第一個步驟是建立 SDO 電腦物件。
ms.assetid: bdb01437-08d0-4279-94f2-840cb786cc44
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf85f9712e76bbdadcffa3914a86cc56576aecd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023727"
---
# <a name="obtaining-a-machine-sdo"></a>取得電腦 SDO

使用 SDO API 的第一個步驟是建立 SDO 電腦物件。

您可以使用 [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) 函式來取得 SDO 電腦物件 (CLSID) 的類別識別碼。 用於物件 (ProgID) 的程式設計識別碼是「IAS」。SdoMachine".

有了 CLSID 之後，請使用此 CLSID 呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 。 將 [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) 指定為要傳回指標的介面。

請參閱 [附加至 SDO-Enabled 電腦](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) ，取得示範如何取得電腦 SDO 的範例程式碼。

 

 