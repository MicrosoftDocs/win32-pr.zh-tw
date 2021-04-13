---
description: Direct3D 會維持最多8個目前材質的清單。 它會將這些材質混合到其呈現的所有基本型別。 只有建立為材質介面指標的紋理，才能在目前的材質集中使用。
ms.assetid: 5a58c915-7b67-45a7-9493-6657c75aaa10
title: '將目前的材質指派 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7ae6d603d9547841628f9395889095533cf3e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468577"
---
# <a name="assigning-the-current-textures-direct3d-9"></a>將目前的材質指派 (Direct3D 9) 

Direct3D 會維持最多8個目前材質的清單。 它會將這些材質混合到其呈現的所有基本型別。 只有建立為材質介面指標的紋理，才能在目前的材質集中使用。

應用程式會呼叫 [**IDirect3DDevice9：： SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 方法，將材質指派給目前材質的集合。 第一個參數必須是0-7 （含）範圍內的數位。 傳遞紋理介面指標做為第二個參數。

下列 c + + 程式碼範例會示範如何將材質指派給目前的材質集。


```
// This code example assumes that the variable lpd3dDev is a
// valid pointer to an IDirect3DDevice9 interface and pTexture
// is a valid pointer to an IDirect3DBaseTexture9 interface.

// Set the third texture.
d3dDevice->SetTexture(2, pTexture);
```



> [!Note]  
> 軟體裝置不支援一次將材質指派給一個以上的材質階段。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質混色](texture-blending.md)
</dt> </dl>

 

 
