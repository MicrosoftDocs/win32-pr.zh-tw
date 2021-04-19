---
description: 位址篩選器會通知網路監視器驅動程式，接受具有其中一種指定 MAC 網址類別型的框架 (乙太網路、權杖響鈴和 FDDI) 。
ms.assetid: 23a38f49-2d63-4fc8-8113-29143493359c
title: 寫入 ADDRESSTABLE 篩選部分
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b06b00d046d555dffc39561b817629f4f47ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978364"
---
# <a name="writing-addresstable-filter-portion"></a>寫入 ADDRESSTABLE 篩選部分

位址篩選器會通知網路監視器驅動程式，接受具有其中一種指定 MAC 網址類別型的框架 (乙太網路、權杖響鈴和 FDDI) 。 您可以指定最多8個位址配對。 位址組可以指定來源、目的地、兩者或兩者皆非。

篩選器的位址部分是由兩個結構所組成： [**ADDRESSTABLE**](addresstable.md) 和 [**ADDRESSPAIR**](addresspair.md)。

如果您沒有指定位址，則所有畫面格都會通過位址篩選。 但是，如果您指定任何位址，則只有通過指定位址篩選的框架才會通過。

建立位址篩選牽涉到配置 [**ADDRESSTABLE**](addresstable.md) 結構，以及填入 [**ADDRESSPAIR**](addresspair.md) 結構的成員。

**若要建立 capture 篩選器的位址部分**

1.  使用 [**CAPTUREFILTER**](capturefilter.md)結構的 **CAPTUREFILTER \_ 旗標 \_ 本機 \_ 旗標**，將捕捉限制在本機電腦的進出流量。

    設定此旗標不會將 NIC 設定為混合模式;capture 檔案只會捕獲本機流量。

2.  使用下列範例程式碼來定義 [**ADDRESSTABLE**](addresstable.md) 結構：

    ``` syntax
    typedef struct _ADDRESSTABLE
    {
        DWORD           nAddressPairs;
        DWORD           nNonMacAddressPairs;
        ADDRESSPAIR     AddressPair[MAX_ADDRESS_PAIRS];
    } ADDRESSTABLE;

    typedef ADDRESSTABLE *LPADDRESSTABLE;
     
    typedef struct _ADDRESSPAIR
    {
        WORD        AddressFlags;
        WORD        NalReserved;
        ADDRESS     DstAddress;
        ADDRESS     SrcAddress;
    } ADDRESSPAIR;

    typedef ADDRESSPAIR *LPADDRESSPAIR;
    ```

3.  使用下表所列的資訊，來選取 [**ADDRESSPAIR**](addresspair.md) 旗標類型。 

    | 旗標                             | 意義                                                                               |
    |----------------------------------|---------------------------------------------------------------------------------------|
    | 位址 \_ 旗標 \_ 符合 \_ DST       | 符合目的地位址。                                                        |
    | 位址 \_ 旗標 \_ 符合 \_ SRC       | 符合來源位址                                                              |
    | 位址 \_ 旗標 \_ 排除          | 如果找到此位址 (定義的來源或目的地) ，則排除框架。 |
    | 位址 \_ 旗標 \_ DST \_ 群組 \_ 位址 | 比對目的地位址的群組位 (，) 只適用于廣播類型的訊息。      |
    | \_ \_ 符合兩者的位址旗標 \_      | 符合目的地和來源位址。                                    |

    

     

4.  填入目的地位址，該位址會針對您選取的 [**ADDRESSPAIR**](addresspair.md) 旗標進行評估。
5.  填入來源位址，該位址會針對您選取的 [**ADDRESSPAIR**](addresspair.md) 旗標進行評估。
6.  以 [**ADDRESSPAIR**](addresspair.md)結構的陣列填入 [**ADDRESSTABLE**](addresstable.md)結構，其中包含驅動程式所評估的位址組。 所有位址組都會評估為邏輯 OR 語句 (ADDRESSPAIR 1 \| \| ADDRESSPAIR 2) 。 您最多可以在捕獲篩選中包含八個位址組。

 

 



