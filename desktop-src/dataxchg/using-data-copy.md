---
title: 使用資料複製
description: 本主題提供的範例會示範如何在兩個應用程式之間傳送資訊。
ms.assetid: 5b37aa75-1208-435b-bf81-3e75f48f27f3
keywords:
- Windows 消費者介面，資料複製
- 資料複製，範例
- 資料複製，WM_COPYDATA 訊息
- WM_COPYDATA 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e44c4abb9aba68d4db1544f5c7d52220cdc681
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106979668"
---
# <a name="using-data-copy"></a><span data-ttu-id="5aee1-107">使用資料複製</span><span class="sxs-lookup"><span data-stu-id="5aee1-107">Using Data Copy</span></span>

<span data-ttu-id="5aee1-108">下列範例示範如何在兩個使用 [**WM \_ COPYDATA**](wm-copydata.md) 訊息的應用程式之間傳送資訊。</span><span class="sxs-lookup"><span data-stu-id="5aee1-108">The following example demonstrates how to send information between two applications using the [**WM\_COPYDATA**](wm-copydata.md) message.</span></span>

<span data-ttu-id="5aee1-109">傳送應用程式會向使用者顯示要求特定資訊的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="5aee1-109">The sending application displays a dialog box to the user which requests certain information.</span></span> <span data-ttu-id="5aee1-110">應用程式會將資訊封裝成私用資料結構，在 [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) 結構中包含結構的指標，並使用 [**WM \_ COPYDATA**](wm-copydata.md) 訊息將資訊傳送至接收應用程式。</span><span class="sxs-lookup"><span data-stu-id="5aee1-110">The application packages the information into a private data structure, includes a pointer to the structure in the [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) structure, and sends the information to the receiving application using the [**WM\_COPYDATA**](wm-copydata.md) message.</span></span> <span data-ttu-id="5aee1-111">接收應用程式的隱藏視窗具有類別名稱 Disp32Class。</span><span class="sxs-lookup"><span data-stu-id="5aee1-111">The receiving application has a hidden window with the class name Disp32Class.</span></span>


```C++
// ************ Globals ************
//
#define MYDISPLAY 1
typedef struct tagMYREC
{
   char  s1[80];
   char  s2[80];
   DWORD n;
} MYREC;
COPYDATASTRUCT MyCDS;
MYREC MyRec;
HRESULT hResult;
BOOL CALLBACK InfoDlgProc( HWND, UINT, WPARAM, LPARAM );
// ************ Code fragment ****************
// Get data from user. InfoDlgProc stores the information in MyRec.
//
   DialogBox( ghInstance, "InfoDlg", hWnd, (DLGPROC) InfoDlgProc );
//
// Copy data into structure to be passed via WM_COPYDATA.
// Also, we assume that truncation of the data is acceptable.
//
   hResult = StringCbCopy( MyRec.s1, sizeof(MyRec.s1), szFirstName );
   if (hResult != S_OK)
        return False;
   hResult = StringCbCopy( MyRec.s2, sizeof(MyRec.s2), szLastName );
   if (hResult != S_OK)
        return False;
   MyRec.n = nAge;
//
// Fill the COPYDATA structure
// 
   MyCDS.dwData = MYPRINT;          // function identifier
   MyCDS.cbData = sizeof( MyRec );  // size of data
   MyCDS.lpData = &MyRec;           // data structure
//
// Call function, passing data in &MyCDS
//
   hwDispatch = FindWindow( "Disp32Class", "Hidden Window" );
   if( hwDispatch != NULL )
      SendMessage( hwDispatch,
                   WM_COPYDATA,
                   (WPARAM)(HWND) hWnd,
                   (LPARAM) (LPVOID) &MyCDS );
   else
      MessageBox( hWnd, "Can't send WM_COPYDATA", "MyApp", MB_OK );
```



<span data-ttu-id="5aee1-112">接收應用程式有隱藏的視窗，它會接收來自 [**WM \_ COPYDATA**](wm-copydata.md) 的資訊，並向使用者顯示該資訊。</span><span class="sxs-lookup"><span data-stu-id="5aee1-112">The receiving application has a hidden window which receives the information from [**WM\_COPYDATA**](wm-copydata.md) and displays it to the user.</span></span>


```C++
// ************ Globals ************
//
#define MYDISPLAY 1
typedef struct tagMYREC
{
   char  s1[80];
   char  s2[80];
   DWORD n;
} MYREC;
PCOPYDATASTRUCT pMyCDS;
void WINAPI MyDisplay( LPSTR, LPSTR, DWORD );
//
// ************ Code fragment ****************
//
case WM_COPYDATA:
   pMyCDS = (PCOPYDATASTRUCT) lParam;
   switch( pMyCDS->dwData )
   {
      case MYDISPLAY:
         MyDisplay( (LPSTR) ((MYREC *)(pMyCDS->lpData))->s1,
                    (LPSTR) ((MYREC *)(pMyCDS->lpData))->s2,
                    (DWORD) ((MYREC *)(pMyCDS->lpData))->n );
   }
   break;
```



## <a name="related-topics"></a><span data-ttu-id="5aee1-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="5aee1-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5aee1-114">**參考**</span><span class="sxs-lookup"><span data-stu-id="5aee1-114">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5aee1-115">**FindWindow**</span><span class="sxs-lookup"><span data-stu-id="5aee1-115">**FindWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-findwindowa)
</dt> </dl>

 

 