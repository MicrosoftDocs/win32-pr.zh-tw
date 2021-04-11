---
description: 資料物件具有下列語法定義。
ms.assetid: e636c2eb-3c11-45bf-ab0b-a14ec878742c
title: '資料 (X 檔案格式) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efdf799b9f7f155c8d2a0e883c8d5e79f8091156
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108412"
---
# <a name="data-x-file-format-binary-encoding"></a><span data-ttu-id="b9817-103">資料 (X 檔案格式，二進位編碼) </span><span class="sxs-lookup"><span data-stu-id="b9817-103">Data (X file format, binary encoding)</span></span>

<span data-ttu-id="b9817-104">資料物件具有下列語法定義。</span><span class="sxs-lookup"><span data-stu-id="b9817-104">A data object has the following syntax definition.</span></span>


```
object                : identifier optional_name TOKEN_OBRACE
                            optional_class_id
                            data_parts_list
                            TOKEN_CBRACE

data_parts_list       : data_part
                      | data_parts_list data_part

data_part             : data_reference
                      | object
                      | number_list
                      | float_list
                      | string_list

number_list           : TOKEN_INTEGER_LIST

float_list            : TOKEN_FLOAT_LIST

string_list           : string_list_1 list_separator

string_list_1         : string
                      | string_list_1 list_separator string

list_separator        : comma
                      | semicolon

string                : token_string

identifier            : name
                      | primitive_type

data_reference        : TOKEN_OBRACE name optional_class_id TOKEN_CBRACE
```



<span data-ttu-id="b9817-105">請注意，在數位 \_ 清單和浮點數 \_ 清單中，二進位檔案中的資料 \_ 不會使用標記逗號和標記 \_ 分號。</span><span class="sxs-lookup"><span data-stu-id="b9817-105">Note that in number\_list and float\_list data in binary files, TOKEN\_COMMA and TOKEN\_SEMICOLON are not used.</span></span> <span data-ttu-id="b9817-106">字串清單資料中會使用逗號和分號 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b9817-106">The comma and semicolon are used in string\_list data.</span></span> <span data-ttu-id="b9817-107">另請注意，您只能將資料 \_ 參考用於選擇性的資料成員。</span><span class="sxs-lookup"><span data-stu-id="b9817-107">Also note that you can only use data\_reference for optional data members.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9817-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="b9817-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9817-109">二進位編碼方式</span><span class="sxs-lookup"><span data-stu-id="b9817-109">Binary Encoding</span></span>](binary-encoding.md)
</dt> </dl>

 

 



