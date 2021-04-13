---
description: 使用逗號和分號可能是最複雜的檔案格式語法問題，而這種用法非常嚴格。 逗號可用來分隔陣列成員;分號會終止每個資料項目。
ms.assetid: 82582213-907c-4760-a849-e6cf5f6d60bc
title: 使用逗號和分號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba238d50ff5d0dace017f16b75547df6b016e14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109881"
---
# <a name="use-of-commas-and-semicolons"></a>使用逗號和分號

使用逗號和分號可能是最複雜的檔案格式語法問題，而這種用法非常嚴格。 逗號可用來分隔陣列成員;分號會終止每個資料項目。

例如，如果範本是以下列方式定義：


```
template mytemp {
DWORD myvar;
}
```



然後，此範本的實例看起來如下所示：


```
mytemp dataTemp {
1;
}
```



如果範本包含另一個範本，則會以下列方式定義：


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
FLOAT aFloat;
mytemp aTemp;
}
```



然後，此範本的實例看起來如下所示：


```
container dataContainer {
1.1;
2; 
3;;
}
```



請注意，代表容器內 mytemp 的第二行在行尾有兩個分號。 第一個分號表示資料項目的結尾，aTemp (在容器) 內，而第二個分號表示容器的結尾。

如果陣列是以下列方式定義：


```
Template mytemp {

array DWORD myvar[3];

}
```



然後，它的實例看起來如下所示：


```
mytemp aTemp {
1, 2, 3;
}
```



在陣列範例中，資料項目目不需要以分號分隔，因為它們是以逗號分隔。 結尾的分號會標示陣列的結尾。

請考慮包含範本所定義之資料項目陣列的範本。


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
DWORD count;
array mytemp tempArray[count];
}
```



這種情況的實例看起來會如下列範例所示。


```
container aContainer {
3;
1;2;,3;4;,5;6;;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[文字編碼方式](text-encoding.md)
</dt> </dl>

 

 



