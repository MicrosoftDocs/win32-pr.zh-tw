---
description: 許多 c + + 應用程式會先清除深度緩衝區，再呈現每個新的框架。
ms.assetid: b8930211-82a1-4808-b042-1641e567cb6d
title: " (Direct3D 9) 清除深度緩衝區"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce150d729768321cb51abbea9f24ba8b490b7705f35945a4fd03e2a8ed58a039
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989308"
---
# <a name="clearing-depth-buffers-direct3d-9"></a> (Direct3D 9) 清除深度緩衝區

許多 c + + 應用程式會先清除深度緩衝區，再呈現每個新的框架。 您可以藉由呼叫 [**IDirect3DDevice9：： clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) 並針對 Flags 參數指定 D3DCLEAR ZBUFFER，以明確清除透過 Direct3D 的深度緩衝區 \_ 。 **IDirect3DDevice9：： Clear** 方法可讓您在 Z 參數中指定任意深度的值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[深度緩衝區](depth-buffers.md)
</dt> </dl>

 

 
