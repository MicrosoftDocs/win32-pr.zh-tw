---
title: 存取不透明的指標
description: 用戶端可以使用不透明的指標來存取儲存在目的地的資訊。
ms.assetid: 1f6af84f-c6c9-4091-8e6b-2c773541ca97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a3435fd468b41c70105b0b239b35fe24212a7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507308"
---
# <a name="accessing-opaque-pointers"></a>存取不透明的指標

用戶端可以使用不透明的指標來存取儲存在目的地的資訊。 若要使用此儲存體，用戶端必須先呼叫 [**RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) 來取得指標。 每當需要變更資訊時，用戶端必須先呼叫 [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) ，並將 *LockDest* 參數設為 **TRUE**，以鎖定目的地。 一旦鎖定目的地之後，用戶端就可以進行必要的變更。 您可以使用對 **RtmLockDestination** 的另一個呼叫來解除鎖定目的地，並將 *LockDest* 參數設定為 **FALSE**。

[**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination)函式也可讓用戶端使用 *獨佔* 參數，以使用讀取鎖定或寫入鎖定。 用戶端只有在對使用不透明指標所保留的資訊進行變更時，才應該使用寫入鎖定。 用戶端可以使用讀取鎖定來查看儲存在目的地中的不透明指標資訊。

如需示範如何使用這些函數的範例程式碼，請參閱 [存取目的地中的不透明指標](access-the-opaque-pointer-in-a-destination.md)。

 

 




