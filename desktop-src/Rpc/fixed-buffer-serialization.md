---
title: 固定緩衝區序列化
description: 修正緩衝區序列化。
ms.assetid: 3432f468-89f2-48e2-8d86-15ba549f0fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87e3cad0a272ccd493cf9088fedeb272f1206b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372268"
---
# <a name="fixed-buffer-serialization"></a>固定緩衝區序列化

使用固定的緩衝區樣式時，請指定夠大的緩衝區來容納編碼 (封送處理以控制碼執行的) 作業。 當您進行封送時，您會提供包含要解碼之所有資料的緩衝區。

序列化的固定緩衝區樣式使用下列常式：

-   [**MesEncodeFixedBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

**MesEncodeFixedBufferHandleCreate** 函式會配置編碼控制碼所需的記憶體，然後將它初始化。 應用程式可以呼叫 [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) 來重新初始化控制碼，也可以呼叫 [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) 來釋放控制碼的記憶體。 若要建立對應于固定樣式（編碼控制碼）的解碼控制碼，您必須使用 [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)。

應用程式會呼叫 [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) 來釋放編碼或解碼緩衝區控制碼。

## <a name="examples-of-fixed-buffer-encoding"></a>固定緩衝區編碼的範例

下一節提供如何使用固定緩衝區樣式的範例–序列化進程編碼的控制碼。

``` syntax
/*This is a fragment of the IDL file defining MooProc */

...
void __RPC_USER
MyProc( [in] handle_t Handle, [in,out] MyType * pMyObject,
        [in, out] ThisType * pThisObject);
...

/*This is an ACF file. MyProc is defined in the IDL file */

[
    explicit_handle
]
interface regress
{
    [ encode,decode ] MyProc();
}
```

下列摘要表示應用程式的一部分。

``` syntax
if (MesEncodeFixedBufferHandleCreate (
        Buffer, BufferSize, 
        pEncodedSize, &Handle) == RPC_S_OK)
{
    ...
    /* Manufacture a MyObject and a ThisObject */
    ...
    /* The serialization works from the beginning of the buffer because 
   the handle is in the initial state. The function MyProc does the    
   following when called with an encoding handle:
     - sizes all the parameters for marshalling,
     - marshalls into the buffer (and sets the internal state 
    appropriately) 
    */

    MyProc ( Handle, pMyObject, pThisObject );
    ...
    MesHandleFree ();
}
if (MesDecodeBufferHandleCreate (Buffer, BufferSize, &Handle) ==
    RPC_S_OK)
{

    /* The MooProc does the following for you when called with a decoding 
    handle:
     - unmarshalls the objects from the buffer into *pMooObject and 
       *pBarObject
*/

MyProc ( Handle, pMyObject, pThisObject);
...
MesHandleFree ( Handle );
}
```

下一節提供如何使用固定緩衝區樣式的範例–序列化類型編碼的控制碼。

``` syntax
/* This is an ACF file. MyType is defined in the IDL file */

[    
    explicit_handle
]
interface regress
{
    typedef [ encode,decode ] MyType;
}
```

下列摘要表示相關的應用程式片段。


```C++
if (MesEncodeFixedBufferHandleCreate (Buffer, BufferSize, 
    pEncodedSize, &Handle) == RPC_S_OK)
{
    //...
    /* Manufacture a MyObject and a pMyObject */
    //...
    MyType_Encode ( Handle, pMyObject );
    //...
    MesHandleFree ();
}
if (MesDecodeBufferHandleCreate (Buffer, BufferSize, &Handle) ==
    RPC_S_OK )
{
    MooType_Decode (Handle, pMooObject);
    //...
    MesHandleFree ( Handle );
}
```



 

 




