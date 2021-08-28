---
description: 若要在 C 和 Visual Basic .net 中建立 Tablet pc 應用程式 \# ，Microsoft Visual Studio .net 中的專案必須包含 Tablet pc 受管理程式庫元件的參考。 這可讓您存取 managed 物件模型和控制項。
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: '受管理的程式庫和控制項 (Tablet PC) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b4096ba54d3cd882b3ee50469d94792b4a46ce
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884275"
---
# <a name="managed-library-and-controls-tablet-pc"></a>受管理的程式庫和控制項 (Tablet PC) 

若要在 C 和 Visual Basic .net 中建立 Tablet pc 應用程式 \# ，Microsoft Visual Studio .net 中的專案必須包含 Tablet pc 受管理程式庫元件的參考。 這可讓您存取 managed 物件模型和控制項。

## <a name="microsoft-visual-c-and-visual-basicnet"></a>Microsoft Visual C \# 和 Visual Basic .net

在 Windows Vista 中，Tablet PC managed 程式庫元件預設會安裝在兩個目錄中：

-   &lt;systemdrive &gt; ： \\ Program files \\ 一般檔案 \\ Microsoft 共用 \\ 筆墨目錄
-   &lt;systemdrive &gt; ： \\ Program Files \\ Microsoft sdk \\ Windows \\ v 6.0 \\ Bin

若要在 Microsoft Visual Studio .net 中新增 Tablet PC 平臺受控程式庫的參考：

1.  開啟您的 Visual Studio .net 專案。
2.  在 [專案] 功能表上，按一下 [加入參考]。
3.  在 [**加入參考**] 對話方塊的 [ **.net** ] 索引標籤上，選取 [元件] 清單中的 [ **Microsoft Tablet PC API**]。
4.  按一下 [ **選取**]，然後按一下 **[確定]**。

若要在 Visual Studio .net 中加入筆墨分析 api 的參考：

1.  開啟您的 Microsoft Visual Studio .net 專案。
2.  在 [專案] 功能表上，按一下 [加入參考]。
3.  在 [**加入參考**] 對話方塊的 [ **.net** ] 索引標籤上，選取 [元件] 清單中的 [ **Microsoft Tablet PC 筆墨分析 Managed 程式庫**]。
4.  按一下 [ **選取**]，然後按一下 **[確定]**。

> [!Note]  
> 在 Visual Studio 2005 編譯使用 Microsoft 的應用程式時，您必須選取 [ **Project**]、[選取 **屬性**]、選取 [**組建**] 和 [設定平臺目標 = x86]。 此選項不適用於 Microsoft Visual Studio Express 產品。

 

 

 



