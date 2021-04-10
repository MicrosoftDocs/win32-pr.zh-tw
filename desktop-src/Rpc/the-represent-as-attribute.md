---
title: Represent_as 屬性
description: '\ 代表 \_ as \ 屬性可讓您指定特定可資料類型如何呈現給應用程式。'
ms.assetid: 6f07ab90-b5bb-48ae-870c-5abaf80ce0e5
keywords:
- 遠端程序呼叫 RPC、屬性、represent_as
- represent_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7121925f1407cb3390c3ef1e7e5f2f6430506071
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093183"
---
# <a name="the-represent_as-attribute"></a>表示 \_ 為屬性

[ \[ [表示 \_ 為](/windows/desktop/Midl/represent-as)] \] 屬性可讓您指定特定的可資料類型如何呈現給應用程式。 這是藉由針對已知的可類型指定表示類型的名稱，並提供轉換常式來完成。 您也必須提供常式，才能釋放資料類型物件所使用的記憶體。

使用 **\[ 代表 \_ as \]** 屬性來呈現具有不同可能 untransmittable 資料類型的應用程式，而不是實際在用戶端與伺服器之間傳輸的類型。 在 MIDL 編譯時，應用程式所操作的類型也可能是未知的。 當您選擇定義完善的可類型時，您不需要擔心在異類環境中的資料標記法。 **\[ 代表 \_ as \]** 屬性可以藉由減少透過網路傳輸的資料量，讓您的應用程式更有效率。

**\[ 代表 \_ as \]** 屬性類似于 \[ [傳輸 \_ 為](/windows/desktop/Midl/transmit-as) \] 屬性。 不過，當 **\[ 傳輸 \_ 為 \]** 可讓您指定將用於傳輸的資料類型時， **\[ 表示 \_ 為 \]** 可讓您指定如何為應用程式表示資料類型。 不需要在 MIDL 處理的檔案中定義表示的類型;您可以在使用 C 編譯器編譯存根的時候定義它。 若要這樣做，請使用 [應用程式佈建檔 ](the-application-configuration-file-acf-.md) 中的 include 指示詞 (ACF) 編譯適當的標頭檔。 例如，下列 ACF 會針對 **名為 \_ type** 的可類型，定義應用程式的本機類型， **repr \_ 類型**：

``` syntax
typedef [represent_as(repr_type) [, type_attribute_list] named_type;
```

下表描述四個程式設計人員提供的常式。



| 常式傳回的值                      | Description                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------|
| **\_ \_ 來自本機的命名類型 \_** | 配置網路類型的實例，並從本機類型轉換為網路類型。      |
| **命名 \_ 為 \_ local 的型別 \_**   | 從網路類型轉換成區欄位型別。                                                    |
| **命名 \_ 類型 \_ 可用 \_ 本機** | 釋出呼叫所配置的記憶體 **\_ \_ 給 \_ 本機** 常式，但無法釋放類型本身。 |
| **命名 \_ 類型 \_ free \_ inst**  | 釋出網路類型 (兩端) 的儲存體。                                                     |



 

除了這四個由程式設計人員提供的常式之外，應用程式也不會操作命名的型別。 應用程式可見的唯一類型是表示的類型。 應用程式會使用所表示的型別名稱，而不是編譯器所產生之原型和存根中的傳送型別名稱。 您必須為雙方提供一組常式。

針對暫時 **命名的 \_ 型** 別物件，存根會呼叫 **名為 \_ type \_ free \_ inst** ，以釋放 **\_ \_ 從 \_ 本機呼叫命名類型** 所配置的任何記憶體。

如果表示的類型是指標或包含指標，則在本機常式的 **命名 \_ 型 \_ \_** 別必須配置記憶體給指標指向 (表示型別物件本身的資料，而存根會以) 的一般方式操作。 若為 \[ [out](/windows/desktop/Midl/out-idl) \] 和 \[ [in](/windows/desktop/Midl/in)、out 的型別（ \] 包含 **\[ 代表 \_** 或其中一個元件的型別），就會針對包含屬性的資料物件，自動呼叫 **指名的型別 \_ \_ free \_ local** 常式。 針對 **\[ in \]** 參數，只有當 **\[ 表示 \_ as \]** 屬性已套用至參數時，才會呼叫 **指名 \_ 型別 \_ free \_ local** 常式。 如果屬性已套用至參數的元件，則不會呼叫 *\* *** \_ 免費的 \_ 本機** 常式。 針對內嵌資料和最多一次的呼叫，不會呼叫釋出的常式， (與最上層屬性) **\[ \] （僅限** 參數）相關。

> [!Note]  
> 您可以將 **\[ 傳輸 \_ as \]** 和 **\[ 表示為屬性（attribute \_ ） \]** 套用至相同的型別。 封送處理資料時，會先套用 **\[ 表示 \_ 為 \]** 類型轉換，然後套用 **\[ 傳輸 \_ 作為 \]** 轉換。 封送資料時，會反轉順序。 因此，當封送處理時， \* **\_ 從 \_ local** 會配置命名型別的實例，並將它從區欄位型別物件轉譯為暫時命名的型別物件。 此物件是用於 \* **\_ \_ xmit** 常式的呈現型別物件。 然後， \* **\_ \_ xmit** 常式會配置傳送的型別物件，並將其從名為) 物件的呈現 (轉譯為傳輸的物件。

 

長整數陣列可以用來表示連結的清單。 如此一來，應用程式就會操作此清單，而當傳輸此類型的清單時，傳輸會使用長整數陣列。 您可以從陣列開始，但使用具有 long 整數的開放式陣列的結構比較方便。 下列範例示範如何執行。

``` syntax
/* IDL definitions */
 
typedef struct_lbox 
{
    long        data;
    struct_lbox *        pNext;
} LOC_BOX, * PLOC_BOX;
 
/* The definition of the local type visible to the application, 
as shown above, can be omitted in the IDL file. See the include 
in the ACF file. */
 
typedef struct_xmit_lbox 
{
    short        Size;
    [size_is(Size)] long DaraArr[];
} LONGARR;
 
void WireTheList( [in,out] LONGARR * pData );
 
/* ACF definitions */
 
/* If the IDL file does not have a definition for PLOC_BOX, you 
can still ready it for C compilation with the following include 
statement (notice that this is not a C include): 
include "local.h";*/
 
typedef [represent_as(PLOC_BOX)] LONGARR;
```

請注意，使用 **LONGARR** 類型的常式原型實際上會以 qps-ploc 方塊的形式顯示在存根檔案中， **以 \_** 取代 **LONGARR** 類型。 存根 c 檔案中的適當存根也是如此 \_ 。

您必須提供下列四個功能：

``` syntax
void __RPC_USER
LONGARR_from_local(
    PLOC_BOX __RPC_FAR * pList,
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr );
 
void __RPC_USER
LONGARR_to_local(
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr,
    PLOC_BOX __RPC_FAR * pList );
 
void __RPC_USER
LONGARR_free_inst(
    LONGARR __RPC_FAR * pDataArr);
 
void __RPC_USER
LONGARR_free_local(
    PLOC_BOX __RPC_FAR * pList );
```

以上所示的常式會執行下列動作：

-   **\_ \_ 本機** 常式的 LONGARR 會計算清單的節點、配置具有 **Sizeof** (**LONGARR**) + Count \* **Sizeof** (**long**) 、將 **Size** 欄位設定為 Count 的 LONGARR 物件，以及將資料複製到 **DataArr** 欄位。
-   **LONGARR \_ 至 \_ local** 常式會建立具有大小節點的清單，並將陣列傳送至適當的節點。
-   **LONGARR \_ free \_ inst** 常式在這種情況下不會釋出任何東西。
-   **LONGARR \_ free \_ local** 常式會釋出列表中的所有節點。

 

 