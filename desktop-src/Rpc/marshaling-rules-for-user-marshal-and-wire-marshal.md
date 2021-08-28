---
title: User_marshal 和 wire_marshal 的封送處理規則
description: 封送處理內嵌指標類型的憑證-DCE 規格需要您在實 \_ UserSize、型別 \_ UserMarshal 和型別 UserUnMarshal 函式時觀察下列限制 \_ 。
ms.assetid: 077cdd1a-9630-459e-8749-ab0c70b16ecb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97f073a5745570aae5c52d4a61d2454b960d77a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883834"
---
# <a name="marshaling-rules-for-user_marshal-and-wire_marshal"></a>封送處理使用者 \_ 封送處理和網路封送處理的規則 \_

封送處理內嵌指標類型的憑證-DCE 規格需要您在實 &lt; &gt; \_ UserSize、 &lt; 型別 &gt; \_ UserMarshal 和 &lt; 型別 &gt; \_ UserUnMarshal 函式時觀察下列限制。  (此處提供的規則和範例適用于封送處理。 不過，您的大小調整和封送送出常式必須遵循相同的限制) ：

-   如果連線類型是沒有指標的一般類型，則對應 userm 類型的封送處理常式應該只會根據網路類型的配置封送處理資料。 例如：

    ``` syntax
    typedef [wire_marshal (long)] void * HANDLE_HANDLE;
    ```

    請注意，網路類型 **long** 是一種平面類型。 只要將控制碼控制碼物件傳遞給控制碼，UserMarshal 函式就 \_ \_ 會封送處理 \_ 。

-   如果連線類型是另一種類型的指標，則對應 userm 型別的封送處理常式應該會根據有線型別所指向之類型的版面配置來封送處理資料。 NDR 引擎負責處理指標。 例如：

    ``` syntax
    typedef struct HDATA
    {
        long size;
        [size_is(size)] long * pData;
    } HDATA;

    typedef HDATA * WIRE_TYPE;
    typedef [wire_marshal(WIRE_TYPE)] void * HANDLE_DATA;
    ```

    請注意，網路類型 [ **電傳 \_ 類型]** 是指標類型。 您的控制碼資料 UserMarshal 函式會 \_ \_ 使用 HDATA 配置（而非 HDATA 配置）來封送處理與控制碼相關的資料 \* 。

-   有線類型必須是一般資料類型或指標類型。 如果您的 transmissible 類型必須是其他 (具有指標的結構，例如) ，請使用您想要的型別指標作為網路類型。

這些限制的影響是以 \[ [**網路 \_ 封送**](/windows/desktop/Midl/wire-marshal)處理 \] 或 \[ [**使用者 \_ 封送**](/windows/desktop/Midl/user-marshal)處理屬性定義的類型 \] 可以自由地內嵌在其他類型中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**網路 \_ 封送處理**](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**使用者 \_ 封送處理**](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[型別 \_ UserSize 函式](the-type-usersize-function.md)
</dt> <dt>

[型別 \_ UserMarshal 函式](the-type-usermarshal-function.md)
</dt> <dt>

[Thetype \_ UserUnMarshalFunction](the-type-userunmarshal-function.md)
</dt> <dt>

[Thetype \_ UserFreeFunction](the-type-userfree-function.md)
</dt> </dl>

 

 
