---
description: 許多 c + + 應用程式會先清除深度緩衝區，再呈現每個新的框架。
ms.assetid: b8930211-82a1-4808-b042-1641e567cb6d
title: " (Direct3D 9) 清除深度緩衝區"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ad415b5c92e62da4f64eb590a0e202ffa3e0c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971314"
---
# <a name="clearing-depth-buffers-direct3d-9"></a> (Direct3D 9) 清除深度緩衝區

許多 c + + 應用程式會先清除深度緩衝區，再呈現每個新的框架。 您可以藉由呼叫 [**IDirect3DDevice9：： clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) 並針對 Flags 參數指定 D3DCLEAR ZBUFFER，以明確清除透過 Direct3D 的深度緩衝區 \_ 。 **IDirect3DDevice9：： Clear** 方法可讓您在 Z 參數中指定任意深度的值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[深度緩衝區](depth-buffers.md)
</dt> </dl>

 

 
