---
title: IAgent UnLoad
description: IAgent UnLoad
ms.assetid: 560301b3-c038-4c6e-b3f1-1203b618b67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e6e457e2acc33c5b34800b8378d82a50d5c4aa6a139366ca1c0d241f676f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610138"
---
# <a name="iagentunload"></a>IAgent：： UnLoad

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT UnLoad(
   long * dwCharID  //character ID
);
```

從 [**字元**](/windows/desktop/lwef/the-characters-object) 集合中卸載指定字元的字元資料。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

字元的識別碼。

</dd> </dl>

當您不再需要字元時，請使用這個方法來釋出用來儲存字元相關資訊的記憶體。 如果您再次存取此字元，請使用 [**Load**](load-method.md) 方法。

## <a name="see-also"></a>另請參閱

[**IAgent：： Load**](iagent--load.md)


 

 